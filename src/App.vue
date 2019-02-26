<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

const x = {
b: 1,
a: [],
c: {},
d: 2
}
console.log(x)

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  methods: {
foo() {
const x = {
b: 1,
a: [],
c: {},
d: 2
}
console.log(x)
}
  }
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
