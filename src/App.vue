<template>
  <Counter />
  <Twoway />
</template>

<script>
import Counter from './components/Counter.vue'
import Twoway from './components/Twoway.vue'

export default {
  name: 'App',
  components: {
    Counter,
    Twoway
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

div {
  margin: 3rem;
}
</style>
