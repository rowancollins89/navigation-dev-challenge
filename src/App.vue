<template>
  <div id="app">
    <gradient-nav/>
  </div>
</template>

<script>
import RainbowNav from "./components/RainbowNav";
import GradientNav from "./components/GradientNav";

export default {
  name: "App",
  components: {
    RainbowNav,
    GradientNav
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
