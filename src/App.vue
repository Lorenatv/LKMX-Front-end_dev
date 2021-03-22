<template>
  <div id="app">
    <h1 style="margin-left: 2em; font-size:42px;">LKMX-Front-end</h1>
    <div class="container">  
      <img alt="Vue logo" src="./assets/logo.png">
      <h1>To Do List</h1>
      <InputTask/>
      <ListTask/>
    </div>
  </div>
</template>

<script>
import InputTask from './components/InputTask.vue'
import ListTask from './components/ListTask.vue'

export default {
  name: 'App',
  components: {
    InputTask,
    ListTask
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
