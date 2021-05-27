<template>
  <div>
      <img alt="Vue logo" src="./assets/logo.png">
      <editor v-model:value="code" />
  </div>
</template>

<script>
import Editor from './components/Editor.vue'

export default {
  name: 'App',
  components: {
    Editor
  },
  data() {
    return {
        code: [{ "a":10 }]
    }
  },
  watch: {
    code(newValue) {
      console.log('code changes? ', newValue);
    }
  },
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
