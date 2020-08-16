
<template>
  <div class='container'>
    <h1>block header</h1>
      <list v-for="(item,index) in data" :info="item"></list>
    </div>
  </div>
</template>

<script>
import list from "./list"
//import Vue from 'vue'

let info = [{
  order: {name:'orderName',age:90,time:2020},
  list:[
    {price:90,value:3},
    {price:30,value:1},
    {price:23,value:5},
    {price:54,value:2}
  ]},
  {
    order: {name:'orderName_2',age:29,time:2019},
  list:[
    {price:80,value:3},
    {price:70,value:1},
    {price:93,value:1},
    {price:34,value:1}
  ]
}]
export default {
  name: 'app',
  components: {
    list
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      data: '',
      visible: true
    }
  },
  mounted: function() {
    console.log('wrap mounted')
    this.data = info
  }
}
/*new Vue({
  el: '#app',
  render: h => h(app)
})*/

</script>

<style lang="scss">
.container {
  border:1px solid;
  padding:30px;
  &:hover {
    cursor:pointer;
  }
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
