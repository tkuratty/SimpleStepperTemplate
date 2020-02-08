<template>
  <div id="app">
    <simple-stepper></simple-stepper>
  </div>
</template>

<script>
import SimpleStepper from "./components/SimpleStepper";

export default {
  name: "App",
  components: {
    SimpleStepper
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
