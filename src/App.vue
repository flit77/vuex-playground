<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view></router-view>
    <div>
      Counter: {{ $store.state.count }} times, count is {{ evenOrOdd }}.
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  name: 'hello',
  computed: mapGetters([
    'evenOrOdd'
  ])
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
