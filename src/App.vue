<template>
  <div id="app">
    <Button title="click me" @click="toggleShown"/>

    <h1 v-if="shown">{{ msg }}</h1>
  </div>
</template>

<script>
import Button from './components/Button'
import 'normalize.css'

export default {
  name: 'app',
  components: {
    Button
  },
  data() {
    return {
      shown: false,
      msg: 'You clicked THE BUTTON'
    }
  },
  methods: {
    toggleShown() {
      console.log('toggling...')
      this.shown = !this.shown
    }
  }
}
</script>

<style>
  :root {
    --space: 1.25rem;
    --black: hsl(0, 0%, 23%);
    --white: hsl(0, 0%, 95%);
    --font: 'Nunito', sans-serif;
  }

  #app {
    min-height: 100vh;
    background: var(--white);
    color: var(--black);
    font-family: var(--font);
    display: grid;
    align-items: center;
    justify-content: center;
  }
</style>
