<template>
  <div class="home">
    <div
      style="color: #4d4d4d; text-align:center; line-height: 95%; margin:0; padding: 0; font-size:60px; font-weight:700; font-family: helvetica neue, Helvetica, sans-serif;
"
    >
      Thomas Finch.
    </div>

    <br />
    <br />
    <p style="text-align:center; font-size:18px;">
      A Macclesfield based software developer trying to decide where software
      can’t be the solution to the problem.
    </p>

    <br />

    <br />

    <br />
    <br />

    <h3>Here’s Some Stuff I Built (For Fun)</h3>

    <a href="https://github.com/fincht96/asthma-tracker"
      >Asthma Tracking Web App</a
    >
    <p>
      Having been recently required to log my peak expiratory flow (PEF) readings and
      finding that I had to do this, rather inconveniently, on a paper graph,
      basically a giant fold map. I decided to create my own solution.<br />
      A full stack MongoDB, Node and Vue js based solution that enables users to
      sign up, log their daily peak flow readings and visualise their results in
      a graphical format.
    </p>

    <br />

    <a href="https://github.com/fincht96/Flappy-Demo"
      >Multi Layer Neural Network (MLNN) with Genetic Evolution</a
    >
    <p>
      Implemented in Java and Libgdx this project consists of a flappy bird
      clone and a MLNN. To the play the game an array of randomly generated
      birds is first created. Each bird consisted of a MLNN with unique inputs
      and outputs connected to movement controls.<br />The birds then attempt to
      play the game with the game resetting when all birds have died. The birds
      that survive longest during the game are then used to produce the next
      generation improving the fitness of the population in each successive
      generation.
    </p>

    <br />
    <br />

    <h3>What I’m Currently Working On (In my Freetime)</h3>

    <a href="https://github.com/fincht96/technical-trading"
      >Python Trading Bot</a
    >

    <p>
      With some experience investing on the stock market, an interest in
      technical analysis and wanting to make some more money; I decided to
      pursue the idea of creating an algorithmic bot that could invest on my
      behalf.<br />Having recognised Python as the best language for data
      science and machine learning and Yahoo finance as the best source for live
      and historical stock data; I have set about implementing various
      strategies and backtesting to find the optimal investing approach to
      short-medium term investing.
    </p>

    <br />

    <h3>What I’m Currently Working On (At Work)</h3>

    <a>Web Front End and System on Chip (SoC) WiFi Web Server</a>

    <p>
      With the company’s trend towards a more ubiquitous user interfacing
      solution the logical direction was towards a web based solution. To
      facilitate this, I encouraged the integration of web server capable SoC’s
      on our gas detection systems. My role within this project is developing
      both the server and the frontend.<br />
      The server, developed in C++, is a static file server, hosting the
      frontend web pages, and a REST framework, supporting interfacing to the
      microcontroller controlled gas detection systems. Developed primarily
      using Vue js, the front end is a collection of dynamic web pages replacing
      and enhancing the existing user interface functionality in IGD systems.
    </p>

    <br />
    <br />
  </div>
</template>

<script>
//  @ is an alias to /src

export default {
  name: "Home"
};
</script>

<style lang="scss" scoped>
a {
  cursor: pointer;

  font-family: helvetica neue, Helvetica, sans-serif;
  font-weight: 700;
  line-height: 1.25;
  margin-top: 1em;
  margin-bottom: 0.5em;
  color: #4b4b4b;

  text-decoration: none;
  /* opacity: 50%; */
  font-size: 18px;
  box-sizing: border-box;
}

.home {
  display: flex;

  flex-direction: column;
  width: 100%;
  max-width: 800px;
  text-align: left;

  margin: 0 auto;
}

.title {
  font-family: "Montserrat", sans-serif;
}
</style>
