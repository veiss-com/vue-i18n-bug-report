<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{$d(new Date(),'short')}}</h1>
    <div class="locale-changer">
      <select v-model="$i18n.locale">
        <option v-for="(lang, i) in langs" :key="`Lang${i}`" :value="lang">{{ lang }}</option>
      </select>
    </div>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return { langs: ['es', 'eu'] }
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
