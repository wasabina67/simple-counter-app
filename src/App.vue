<template>
  <div>
    <button @click="down" class="counter-button">-</button>
    <span class="counter-display">{{ counter }}</span>
    <button @click="up" class="counter-button">+</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    down() {
      this.counter--;
    },
    up() {
      this.counter++;
    },
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
