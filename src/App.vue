<template>
  <div id="app">
    <Navigation></Navigation>
    <router-view class="container" :user="user" />
  </div>
</template>

<script>
import Navigation from "./components/Navigation";
import Firebase from "firebase"
import db from "./db"
export default {
  name: "app",
  components: {
    Navigation
  },data: () => {
    return {
      user: null
    };
  },
  async mounted() {
    const snapshot = await db
      .collection("users")
      .doc("aYg9eL2aarjgQIbe7Xkp")
      .get();

    this.user = snapshot.data().name;
  },
};
</script>

<style lang="scss">
$primary: #3a3a3a;
@import "node_modules/bootstrap/scss/bootstrap";
</style>
