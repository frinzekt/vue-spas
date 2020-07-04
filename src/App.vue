<template>
  <div id="app">
    <Navigation></Navigation>
    <router-view class="container" />
  </div>
</template>

<script>
import Navigation from "./components/Navigation";
export default {
  name: "app",
  components: {
    Navigation
  }
};
</script>

<style lang="scss">
$primary: #3a3a3a;
@import "node_modules/bootstrap/scss/bootstrap";
</style>
