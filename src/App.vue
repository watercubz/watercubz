<script setup>
  import Home from "./components/Home.vue";
  import DarkMode from "./components/DarkModeToggle.vue"
</script>

<template>
  <DarkMode />
   <Home />
</template>

<style>
  :global(::selection) {
    color: #ca9787;
    background-color: #8a817c;
  }

  :global(.text-highlight::selection) {
    color: #757474;
    background-color: #ca9787;
  }
</style>
