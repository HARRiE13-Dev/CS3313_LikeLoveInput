<template>
  <div id="app">
   <img src="./assets/logo.png" alt="">
    <HelloWorld msg="VUE Project Counter & INPUT"/>
    <h3>Surachart Khongkamnert</h3>
    <h4>__________________________________________________</h4><br>
    <p>{{counter}}</p>

<div class="container">
  <div class="row">
    <div class="col-sm">
      <counter label='like'/>
    </div>
  </div>
</div>

<h4>__________________________________________________</h4><br>

<h4>Name <input type="text" v-model ="name"></h4> 
<h4>Code <input type="text" v-model ="code"></h4>
<h4>GPA <input type="number" v-model ="gpa"></h4>

<br>
<h3> - Output -</h3> <br>

<p>{{name}} {{code}} {{gpa}}</p>

  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'
import counter from './components/counter.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    counter
  },


  data:function (){
    return{
      name: "",
      code: "",
      gpa: 0.0

    };
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
