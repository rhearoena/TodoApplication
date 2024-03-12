<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import TodotasksList from './components/TodotasksList.vue';
</script>

<template>
  <div class="relative h-32 w-32 ...">

    
    <div class="absolute inset-y-0 left-0 w-16 ...">
      <nav class="navbar navbar-expand navbar-dark bg-dark">
        
        <!-- <router-link to="/" class="navbar-brand">RheJerVinVie</router-link> -->
        <div class="navbar-nav mr-auto">
          <li class="nav-item">
            <router-link to="/todotasks" class="nav-link">Todotasks</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/addTodotask" class="nav-link">Add</router-link>
          </li>
        </div>
      </nav>
    </div>
  </div>
  <TodotasksList/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
