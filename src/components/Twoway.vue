<template>
  <div>
      <p>{{ message }}</p>
      <input v-model="message">
  </div>
  <div>
      <span v-if="seen">Now you see me</span>
  </div>
  <button v-on:click="hide">Hide</button>
</template>

<script>

export default {
  name: 'Twoway',
  data () {
    return {
      message: 'Manipulate Me!',
      seen: true
    }
  },
  methods: {
    hide () {
      if (this.seen === true) {
        this.seen = false
      }
    }
  }
}
</script>
