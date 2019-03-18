<template>
  <div id="app">
    <Header/>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layout/Header';

export default {
  name:"app",
  components:{
    Header
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

  .btn{
    display:inline-block;
    border:none;
    background:#555;
    color:#fff;
    padding:7px 20px;
    cursor:pointer;
  }

  .btn:hover{
    background:#666;
  }
</style>
