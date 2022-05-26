<template>
  <div id="app">
    <section class="row">
      <div class="small-6 collumns">
        <h1 class="text-center">You</h1>
        <img
          src="./assets/rengoku.png"
          class="img"
          alt=""
          style="width: 100%"
        />

        <div class="healthbar">
          <div
            class="healthbar text-center"
            style="background-color: red; margin: 0; color: white"
            :style="{ width: playerHealth + '%' }"
          >
            {{ playerHealth }}
          </div>
        </div>
      </div>
      <div class="small-6 collumns">
        <h1 class="text-center">Demon</h1>
        <img src="./assets/akaza.png" class="img" alt="" style="width: 100%" />

        <div class="healthbar">
          <div
            class="healthbar text-center"
            style="background-color: red; margin: 0; color: white"
            :style="{ width: monsterHealth + '%' }"
          >
            {{ monsterHealth }}
          </div>
        </div>
      </div>
    </section>
    <section class="row controls" v-if="!gameIsRunning">
      <div class="small-12 collumns">
        <button id="start-game" @click="gameIsRunning = !gameIsRunning">
          START NEW GAME
        </button>
      </div>
    </section>
    <section class="row controls" v-else>
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
    return {
      playerHealth: 100,
      monsterHealth: 100,
      gameIsRunning: false,
    };
  },
  methods: {},
};
</script>

<style>
* {
  box-sizing: border-box;
}
.row {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
}
.img {
  flex: 0 0 50%;
  max-width: 340px;
  object-fit: cover;
  min-height: 486px;
}
.small-6 .collumns {
  min-height: 600px;
}
.text-center {
  text-align: center;
}
.healthbar {
  width: 80%;
  height: 40px;
  background-color: red;
  margin: auto;
  transition: width 500ms;
}
.controls,
.log {
  margin-top: 30px;
  text-align: center;
  padding: 10px;
  border: 1px solid #ccc;
  box-shadow: 0px 3px 6px #ccc;
}

.turn {
  margin-top: 20px;
  margin-bottom: 20px;
  font-weight: bold;
  font-size: 22px;
}
.log ul {
  list-style: none;
  font-weight: bold;
  text-transform: uppercase;
}
.log ul .player-turn {
  color: blue;
  background-color: #e4e8ff;
}
button {
  font-size: 20px;
  background-color: #eee;
  padding: 12px;
  box-shadow: 0 1px 1px black;
  margin: 10px;
}
#start-game {
  background-color: #aaffb0;
}
#start-game:hover {
  background-color: #76ff7e;
}
#attack {
  background-color: #ff7367;
}
#attack:hover {
  background-color: #ff3f43;
}
#special-attack {
  background-color: #ffaf4f;
}
#special-attack:hover {
  background-color: #ff9a2b;
}
#heal {
  background-color: #aaffb0;
}
#heal:hover {
  background-color: #76ff7e;
}
#give-up {
  background-color: #fff;
}
#give-up:hover {
  background-color: #c7c7c7;
}
</style>
