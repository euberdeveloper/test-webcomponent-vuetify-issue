<template>
  <v-app class="app">
    <v-main>
      <group-card />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import vuetify from "@/plugins/vuetify";

import { VApp, VMain } from "vuetify/lib";
import GroupCard from "@/components/group-card/GroupCard.vue";

@Component({
  vuetify,
  components: {
    VApp,
    VMain,
    GroupCard,
  },
})
export default class PncGroupRegistration extends Vue {
}
</script>

<style lang="scss">
@import "vuetify/dist/vuetify.min.css";
</style>

<style lang="scss">
// This is because vuetify uses rem, so to make it behave everywhere the same I set the root font-size
:host {
  font-size: 100px !important;
}
</style>

<style lang="scss">
.app {
  text-align: left;
  max-width: 440px;

  // This is because otherwise the component would get all the height of the screen
  .v-application--wrap {
    height: auto !important;
    min-height: auto !important;
  }
}
</style>