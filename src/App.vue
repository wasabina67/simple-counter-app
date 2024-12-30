<template>
  <div>
    <button @click="down" class="counter-button" :disabled="counter === 0">-</button>
    <span class="counter-display">{{ counter }}</span>
    <button @click="up" class="counter-button" :disabled="counter === 99">+</button>
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
    up() {
      if (this.counter < 99) this.counter++;
    },
    down() {
      if (this.counter > 0) this.counter--;
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

.counter-button {
  font-size: 24px;
  padding: 10px 20px;
  margin: 10px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  border-radius: 5px;
  cursor: pointer;
  user-select: none;
}

.counter-button:hover {
  background-color: #e0e0e0;
}

.counter-display {
  font-size: 48px;
  font-weight: bold;
  margin: 0 20px;
  display: inline-block;
  vertical-align: middle;
}
</style>
