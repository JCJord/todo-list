<template>
  <v-app>
    <TheHeader v-if="!['SignUp', 'Login'].includes($route.name)"></TheHeader>
    <v-main><router-view></router-view></v-main>
  </v-app>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import TheHeader from "./components/header/TheHeader.vue";

@Component({
  components: {
    TheHeader,
  },
})
export default class App extends Vue {}
</script>
