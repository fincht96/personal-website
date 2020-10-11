<template>
  <header>
    <div class="spacer" />
    <div
      v-if="showMenu"
      style="position:fixed; top:0; left:0; height:100vh; width:100%; background:#caffbf; z-index:4;"
    ></div>
    <nav style="z-index:5; position:relative;">
      <input
        class="menu-btn"
        type="checkbox"
        id="menu-btn"
        v-model="showMenu"
      />
      <label class="menu-icon" for="menu-btn"
        ><span class="nav-icon"></span
      ></label>

      <ul class="menu">
        <li class="logo">
          <router-link to="/"
            ><img id="igdlogo" src="../assets/logo.png" width="40px"
          /></router-link>
        </li>
        <div v-if="showMenu">
          <li v-on:click="closeMenu()">
            <router-link to="/" class="menu-item">Work</router-link>
          </li>
          <li v-on:click="closeMenu()">
            <router-link to="/about" class="menu-item">About</router-link>
          </li>
        </div>
      </ul>
    </nav>

    <div class="spacer"></div>
  </header>
</template>

<script>
export default {
  name: "Nav"
};
</script>

<style lang="scss" scoped>
.spacer {
  height: 20px;
  width: 100%;
}



nav .menu .menu-item {
  text-align: left;
}

nav .menu {
  clear: both;
  max-height: min-content;
  transition: max-height 0.3s ease-out;
  margin: 0;
  padding: 0;
  list-style: none;
  overflow: hidden;
  box-sizing: border-box;
  color: black;
}

nav .menu .logo {
  top: 10px;
  // left: 50%;
  margin-left: 20px;
  position: absolute;
}

nav .menu-icon {
  padding: 28px 20px;
  position: relative;
  float: right;
  cursor: pointer;
  -webkit-tap-highlight-color: transparent;
}

nav .menu-icon .nav-icon {
  background: black;
  display: block;
  height: 2px;
  width: 18px;
  position: relative;
  transition: background 0.2s ease-out;
}

nav .menu-icon .nav-icon:before {
  background: black;
  content: "";
  display: block;
  height: 100%;
  width: 100%;
  position: absolute;
  transition: all 0.2s ease-out;
  top: 5px;
}

nav .menu-icon .nav-icon:after {
  background: black;
  content: "";
  display: block;
  height: 100%;
  width: 100%;
  position: absolute;
  transition: all 0.2s ease-out;
  top: -5px;
}

// nav .menu-btn:checked ~ .menu {
//   max-height: min-content;
// }

nav .menu-btn:checked ~ .menu-icon .nav-icon {
  background: transparent;
}

nav .menu-btn:checked ~ .menu-icon .nav-icon:before {
  transform: rotate(-45deg);
  top: 0;
}

nav .menu-btn:checked ~ .menu-icon .nav-icon:after {
  transform: rotate(45deg);
  top: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  background-color: #ffff;
  margin: 0;
  padding: 0;
}
body > footer {
  margin-top: auto;
}

header {
  padding: 0;
  margin: 0;
  font-family: Helvetica, sans-serif;

  /* border-bottom: #e6e6e6 solid 2px; */
}

.show {
  display: block;
}

nav {
  margin: 0 auto;
  /* padding: 0 20px; */
  width: 100%;
  max-width: 1100px;
  box-sizing: border-box;

  /* border: solid 1px #f8f9fa; */
}

nav .menu .menu-item {
  color: black;
  opacity: 50% ;
  cursor: pointer;
  display: block;
  padding: 20px;

  font-family: helvetica neue, Helvetica, sans-serif;
  font-weight: 700;
  line-height: 1.25;
  margin-top: 1em;
  margin-bottom: 0.5em;
  //   color: black;

  text-decoration: none;

  font-size: 30px;
  box-sizing: border-box;
  text-align: center;
}

nav .menu .menu-item:hover {
  opacity: 100%;
}

nav .menu-btn {
  display: none;
}

.router-link-exact-active {
  opacity: 100% !important;
}
</style>


<script>
export default {
  name: "Nav",

  watch: {
    showMenu: function(newVal, oldVal) {
      console.log(newVal);
    }
  },

  methods: {
    closeMenu() {
      console.log("called");
      this.showMenu = false;
    }
  },

  data: function() {
    return {
      showMenu: false
    };
  }
};
</script>

