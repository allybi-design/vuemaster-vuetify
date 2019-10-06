<template>
  <div>
    <v-app-bar app color="deep-purple accent-4" dark>
      <v-img
        src="../assets/logo.png"
        aspect-ratio="1"
        max-width="48"
        max-height="48"
      ></v-img>

      <v-toolbar-title>Vue Mastery - Vuetify</v-toolbar-title>
      <div class="flex-grow-1"></div>
      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen" />
    </v-app-bar>

    <v-navigation-drawer
      dark
      right
      app
      v-model="isDrawerOpen"
      temporary
      class="deep-purple accent-4"
    >
      <v-list>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      items: [
        { title: "Log In", icon: "fas fa-sign-in-alt" },
        { title: "Register", icon: "fas fa-user-plus" }
      ],
      isDrawerOpen: false,
      isLoggedIn: false
    };
  }
};
</script>
