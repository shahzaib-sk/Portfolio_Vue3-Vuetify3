<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn>
      <v-icon color="#2E8B57" left class="mr-3">fas fa-signature</v-icon>Personal Portfolio
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" :style="{ color: '#2E8B57' }">Home</v-btn>
    <v-btn text @click="scroll('about')" :style="{ color: '#2E8B57'}">About</v-btn>
    <v-btn text @click="scroll('portfolio')" :style="{ color: '#2E8B57' }">Portfolio</v-btn>
    <v-btn text @click="scroll('services')" :style="{ color: '#2E8B57' }">Services</v-btn>
    <v-btn text @click="scroll('page')" :style="{ color: '#2E8B57' }">page</v-btn>
    <v-btn text @click="scroll('biog')" :style="{ color: '#2E8B57' }">blog</v-btn>
    <v-btn text @click="scroll('contact')" :style="{ color: '#2E8B57' }">contact</v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: 'smooth'});
    }
  }
}
</script>

<style>

</style>