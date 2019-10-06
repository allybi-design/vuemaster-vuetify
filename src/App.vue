<template>
  <v-app>
    <Navbar />

    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
  components: {
    Navbar: require("./components/Navbar").default
  },
  data() {
    return {};
  }
};
</script>
