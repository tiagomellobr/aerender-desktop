<template>
  <v-app>
    <NavMenu :toggleConfig="toggleConfig" :showConfig="showConfig" />
    <v-main>
      <SettingsView v-if="showConfig"/>
      <MainView v-if="!showConfig"/>
    </v-main>
  </v-app>
</template>

<script>
import MainView from "./components/MainView";
import SettingsView from "./components/SettingsView";
import NavMenu from "./components/NavMenu";

export default {
  name: 'App',

  components: {
    MainView,
    SettingsView,
    NavMenu
  },

  data: () => ({
    showConfig: false,
  }),

  methods: {
    toggleConfig() {
      this.showConfig = !this.showConfig;
    }
  }
}
</script>
