<template>
  <div id="app">
     <div>
        <Random/>
     </div>
    
  </div>
</template>

<script>
import Random from './components/Random.vue'

export default {
  name: 'App',
  components: {
    Random
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ff0000;
  margin-top: 60px;
}

</style>
