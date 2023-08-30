<script setup>
import { RouterView } from 'vue-router' 
import Navber from './components/Navber.vue';
</script>

<template>
  <header> 
        <Navber/>
  </header>

  <RouterView />
</template>