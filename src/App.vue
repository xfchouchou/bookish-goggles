<template>
  <div id="app">
    <div id="nav" v-show="$route.path !== '/Login'">
      <div class="header">
        <div class="img"></div>
        <!--<img src="assets/menu.png" >-->
      </div>
      <!--<router-link to="/Home">Home</router-link> |-->
      <!--<router-link to="/about">About</router-link>-->
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import '../styles/themes.scss';
  body, html{
    height: 100%;
    margin: 0;
    padding: 0;
  }
#app {
  height: 100%;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  background-color: #fff;
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
  .header{
    display: flex;
    .img{

    }
  }
}
</style>
