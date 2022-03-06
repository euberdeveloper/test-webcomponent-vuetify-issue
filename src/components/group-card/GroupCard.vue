<template>
  <v-card class="group-card mx-auto px-8" color="#26c6da" dark>
    <v-card-title class="pa-2">
      <span class="text-h6 font-weight-light d-flex" style="width: 100%">
        <span>Nome gruppo</span>
        <span class="flex-grow-1" />
        <span class="creation">23/04/1999</span>
      </span>
    </v-card-title>

    <v-card-text class="font-weight-bold px-2">
      <span class="text-h6">"Una descrizione per il gruppo"</span>
    </v-card-text>

    <v-card-actions class="px-2">
      <v-icon class="mr-1">$account</v-icon>
      <span class="subheading">
        <span class="partecipants">3</span>
        <span class="mx-1">/</span>
        <span class="maxPartecipants">23</span>
      </span>

      <v-row align="center" justify="end">
        <v-btn text>
          <span class="group-button">ENROLL</span>
        </v-btn>
      </v-row>
    </v-card-actions>

    <div class="arrow back">
      <v-btn small icon> <v-icon large class="group-icon">$menu-left</v-icon> </v-btn>
    </div>
    <div class="arrow next">
      <v-btn small icon> <v-icon large class="group-icon">$menu-right</v-icon> </v-btn>
    </div>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import { VCard, VCardTitle, VCardText, VCardActions, VIcon, VRow, VBtn } from "vuetify/lib";

@Component({
  components: {
    VCard,
    VCardTitle,
    VCardText,
    VCardActions,
    VIcon,
    VRow,
    VBtn,
  },
})
export default class GroupCard extends Vue {}
</script>

<style lang="scss" scoped>
.group-card {
  .name {
    text-decoration: none;
    color: white;
  }

  .arrow {
    position: absolute;
    top: 0;

    width: 32px;
    height: 100%;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .back {
    left: 0;
  }
  .next {
    right: 0;
  }

  .subheading {
    font-size: .875rem;
  }
}
</style>