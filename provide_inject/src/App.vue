<template>
  <h1> hello</h1>
   <CompA :msg="msg"/> 
  
</template>

<script>
import CompA from './components/CompA.vue'


export default {
  name: 'App',
  components: {
    CompA,
    
}, 
data(){
   return{
msg: "hai"
  }
 },
 
provide(){
  return{
  message:"bye"
  }
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
