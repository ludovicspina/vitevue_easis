<template>
  <div>
    <NavBar/>
    <router-view />
  </div>
</template>

<script>
import { createRouter, createWebHistory } from 'vue-router'
import HomePage from '../src/components/HomePage.vue'
import NavBar from "./components/NavBar.vue";
import './assets/tailwind.css';

const routes = [
  { path: '/home', component: HomePage }
]

const router = createRouter({
  history: createWebHistory(),
  routes
})

export default {
  name: 'App',
  components: {NavBar},
  router
}
</script>


<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>