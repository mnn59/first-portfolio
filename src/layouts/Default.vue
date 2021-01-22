<template>
  <v-app>
    <v-navigation-drawer width="240px" permanent>
      <v-list-item>
        <v-list-item-avatar>
          <!-- <v-img src="../avataaars.png"></v-img> -->
          <v-avatar color="primary" size="56">
            <span class="white--text" style="user-select: none">MN</span>
          </v-avatar>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="title"> Mahdi Niknejad</v-list-item-title>
          <v-list-item-subtitle> Software Developer </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
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

    <!-- <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header> -->
    <v-main>
      <v-container>
        <slot />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Education", icon: "mdi-school" },
        { title: "Projects", icon: "mdi-apps" },
        { title: "Contact", icon: "mdi-message-text" },
        { title: "About", icon: "mdi-account-box" },
      ],
    };
  },
};
</script>



<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>


<style>
.v-application--wrap {
  flex-direction: row;
}
.v-main {
  flex: 1 0;
}
</style>