<template>
  <div id="counter">
    Counter: {{ counter }}
  </div>
  <button v-on:click="stopCounter">Stop Counter</button>
  <div id="bind-attribute">
    <span v-bind:title="message">
      When did I load this page???
    </span>
  </div>
</template>

<script>

let counting

export default {
  name: 'Counter',
  data () {
    return {
      counter: 0,
      message: 'You loaded this page on ' + new Date().toLocaleString()
    }
  },
  mounted () {
    counting = setInterval(() => {
      this.counter++
    }, 1000)
  },
  methods: {
    stopCounter () {
      clearInterval(counting)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
#bind-attribute {
  border: 2px solid black;
  border-radius: 20px;
  padding: 1rem;
  width: 50%;
  margin: 2rem auto;
  cursor: help;
}
</style>
