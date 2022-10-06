<template>
  <h1> A TODO LIST</h1>
  
  <input type = "text" placeholder=" Enter the lists"  
        v-model ="newList" />

<button @click="add"> ➕ </button>
<div>
  <ul >
            <!-- v-bind -->
            <li v-for="(list,index) in lists" :key="index" >
            
                index {{index}} :{{list}}
                </li>
        </ul>

</div>
        

</template>

<script>


export default {
  methods:{
 add(){  
     this.$store.commit('addList')
 },

 
},
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
