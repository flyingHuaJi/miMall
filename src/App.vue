<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
// import storage from './storage/index.js'
export default {
  name: 'App',
  components: {
     
  },
  data() {
    return {

    }
  },

  mounted() {
    // 本地加载请求静态 json 文件的方式
    // this.axios.get('/mock/user/login.json').then((res) =>{
    //   this.res = res;
    // })

    this.axios.get('/user/login').then((res) =>{
      this.res = res;
    })

  },

  methods() {

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
