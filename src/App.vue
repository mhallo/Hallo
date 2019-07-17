<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/whoami">Who am I?</router-link>
    </div>
    <transition name="fade" mode="out-in">
      <router-view/>
    </transition>
    <div id="copyright">
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Obcaecati, quasi alias tempore sit, eligendi voluptatem assumenda vero pariatur modi soluta dolorem dicta aspernatur consectetur facilis eum inventore, magnam fugit est?</p>
    </div>
  </div>
</template>

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
#copyright {
  background-color: rgb(87, 170, 54)
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .4s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>