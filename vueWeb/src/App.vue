
<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
<div>
  <label>OverAir's Test </label><br/>
  <br/>
  <selectTest ref="selectitem"></selectTest>
  <el-button @click="getSelect">获取</el-button>
</div>


    <!--<router-view></router-view>-->
  </div>
</template>

<script>
  import selectTest from './pages/selectTest.vue'

  export default {
    name: 'app',
//    data(){
//    return{
//
//    }
//
//  },
    components:{
      selectTest
    },
  methods:{
      getSelect(){
        console.log(this.$refs.selectitem.selectValue);
        alert(this.$refs.selectitem.selectValue);
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
    margin-top: 60px;
  }
</style>
