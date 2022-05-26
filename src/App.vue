<template>
  <div id="app">
    <section class="row">
      <div class="small-6 collumns">
        <h1 class="text-center">You</h1>
        <img src="./assets/rengoku.png" alt="" style="width: 100%" />

        <div class="healthbar">
          <div
            class="healthbar text-center"
            style="background-color: red; margin: 0; color: white"
          ></div>
        </div>
      </div>
      <div class="small-6 collumns">
        <h1 class="text-center">Demon</h1>
        <img src="./assets/akaza.png" alt="" style="width: 100%" />

        <div class="healthbar">
          <div
            class="healthbar text-center"
            style="background-color: red; margin: 0; color: white"
          ></div>
        </div>
      </div>
    </section>
    <section class="row controls">
      <div class="small-12 collumns">
        <button id="start-game">START NEW GAME</button>
      </div>
    </section>
    <section class="row controls">
      <div class="small-12 collumns">
        <button id="attack">ATTACK</button>
        <button id="special-attack">SPECIAL ATTACK</button>
        <button id="heal">HEAL</button>
        <button id="give-up">GIVE UP</button>
      </div>
    </section>
    <section class="row log">
      <div class="small-12 collumns">
        <ul>
          <li></li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
