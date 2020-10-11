<template>
  <div id="app">
    <Nav />

    <br />
    <router-view class="main" />

    <footer>
      <div class="footer">
        <div>Created by Thomas Finch &#169; 2020</div>
        <br />
        <div></div>
      </div>
    </footer>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "App",
  components: {
    Nav,
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  color: #2e2e2e;
  font-family: "MerriWeather", serif;
  padding: 0;
  margin: 0;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: helvetica neue, Helvetica, sans-serif;
  font-weight: 700;
  line-height: 1.25;
  margin-top: 1em;
  margin-bottom: 0.5em;
  color: #3a4145;
}

h3 {
  display: block;
  font-size: 1.17em;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  font-weight: bold;
  text-align: center;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #3a4145;
    font-family: helvetica neue, Helvetica, sans-serif;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.main {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

.footer {
  margin-top: 100px;
  margin-bottom: 10px;
  padding-top: 20px;
  border-top: 1px solid #e6e6e6;
}

footer {
  margin: 0 auto;
  display: grid;
  max-width: 1000px;
  width: 100%;
}
</style>
