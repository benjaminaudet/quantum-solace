<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app clipped>
      <v-list dense>
        <v-list-item>
          <v-list-item-action>
            <v-icon>mdi-theme-light-dark</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>
              <v-switch v-model="$vuetify.theme.dark" primary label="Dark theme" />
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>QuantumSolace</v-toolbar-title>
    </v-app-bar>
    <v-content>
      <router-view />
    </v-content>
    <v-footer app>
      <span>
        QuantumSolace &copy; 2019 - Made with
        <v-icon>mdi-heart</v-icon>&nbsp;by EPITECH students -
        <a href="https://github.com/davidzeng8/quantum-solace">
          <v-icon medium>fab fa-github</v-icon>
        </a>
      </span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  props: {},
  data: () => ({
    drawer: false
  }),
  created() {
    this.$vuetify.theme.dark = true;
  }
};
</script>

<style lang="scss" scoped>
.gates-list {
  height: 42px;
  width: 70%;
  background: #464646;
}
a {
  text-decoration: none;
}
</style>
