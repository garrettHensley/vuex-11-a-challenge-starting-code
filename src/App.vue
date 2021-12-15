<template>
  <the-header></the-header>
  <button @click="addThing">add a thing</button>
  <router-view></router-view>
</template>

<script>
import TheHeader from './components/nav/TheHeader.vue';

export default {
  components: {
    TheHeader,
  },

  methods: {
    addThing() {
      this.$store.commit('addProductToCart', this.products[0]);
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>
