<template>
  <AboutMe/>
  <h1 class="title">Carpintero/Diseñador</h1>
  <ImageCarousel/>
  
</template>

<script>
import AboutMe from './components/AboutMe.vue'

export default {
  name: 'App',
  components: {
    AboutMe
  }
}
</script>

<style>
html, #app, body {
  height: calc(100% - 2rem);
}

body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  margin: 3rem;
}

a {
  color: white;
  text-decoration: none;
}

.title {
  font-size: 5rem;
  margin: 0;
  margin-left: 3rem;
}

</style>
