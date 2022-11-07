<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <header>

    <div class="wrapper">
      <!-- <HelloWorld msg="You did it!" /> -->
      <NavBar/>

      <!-- <nav id="nav">
        <RouterLink to="/">Home</RouterLink> 
        <RouterLink to="/about">About</RouterLink> 
        <RouterLink to="/hello">Hello</RouterLink> 
        <RouterLink to="/brazil">Brazil</RouterLink>
        
      </nav> -->
    </div>
  </header>
 <div class="container">
  <RouterView />
 </div>

 
</template>

<style scoped>


</style>
