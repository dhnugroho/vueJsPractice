<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <first msg="HEYYYY"></first> -->
    <users></users>
  </div>
</template>

<script>
import first from './components/first'
import users from './components/users'

export default {
  name: 'app',
  components: {
      first, users    
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
