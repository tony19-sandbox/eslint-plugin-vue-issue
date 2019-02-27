<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
const x = {
a: [],
b: 1,
c: {},
d: 2
}
console.log(x) // eslint-disable-line no-console

export default {
name: 'app',
components: {
HelloWorld
},

data() {
const x = {
a: [],
b: 1,
c: {},
d: 2
}
return x;
},

methods: {
foo() {
const x = {
a: [],
b: 1,
c: {},
d: 2
}
return x;
}
},

computed: {
bar() {
const x = {
a: [],
b: 1,
c: {},
d: 2
}
return x;
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
