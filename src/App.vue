<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view></router-view>
    <div class="container">
      <div class="row text-center">
          <h3>Clicked: {{ $store.state.count }} times, count is {{ evenOrOdd }}.</h3>
          <button class="btn btn-success" @click="increment">+</button>
          <button class="btn btn-danger" @click="decrement">-</button>
          <button class="btn" @click="incrementIfOdd">Increment if odd</button>
          <button class="btn" @click="incrementAsync">Increment async</button>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
  name: 'hello',
  computed: mapGetters([
    'evenOrOdd'
  ]),
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
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
