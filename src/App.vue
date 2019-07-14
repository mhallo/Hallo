<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/whoami">Who am I?</router-link>
    </div>
    <fade-transition :duration="200">
      <router-view/>
    </fade-transition>
  </div>
</template>

<script>
import {FadeTransition} from 'vue2-transitions'

export default {
  components:
  {
    FadeTransition
  },
  data() {
    return {
      show:true
    }
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
}
#nav {
  padding: 30px;
  background-color: rgb(202, 202, 55);
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
/* 
body 
{
  background: rgb(233,233,233);
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

html, body
{
  height: calc(100% - 50px);
}

#app
{
  background: #fff;
  width: 50%;
  padding: 30px;
  border-radius: 10px;
  margin: 50px auto 0 auto;
  height: calc(60%-50px);
} */
.fade-move{
    transition: transform .3s ease-out;
  }
</style>