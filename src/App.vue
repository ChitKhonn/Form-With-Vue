<template>

  <div>
    <h1>Form</h1>
    <SignUpVue/>
  </div>
  
</template>

<script>
import SignUpVue from './components/SignUp.vue';

export default {
  name: 'App',
  components: {
    SignUpVue,
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

body {
  background-color: #eee;
  margin: 0;
}
</style>
