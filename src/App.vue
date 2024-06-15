<script setup>
import Home from "./components/Home.vue";
</script>

<template>
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
