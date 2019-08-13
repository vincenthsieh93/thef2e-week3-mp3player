<template>
  <div id="app">
    <Player msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import Player from "./components/Player.vue";

export default {
  name: "app",
  components: {
    Player
  }
};
</script>

<style lang="scss">
@import url(assets/style/reset.css);

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  color: #2c3e50;
  background-color: #38346C;
}
</style>
