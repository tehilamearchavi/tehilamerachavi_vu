<template>
 <div>
<button @click="mytasks">mytasks</button>
<ul id="mytasks">
<li  v-for="currenttask  in currenttasks">{{currenttask}}</li>
</ul>
 </div>
<template>
 <script>
 export default{
     data(){
         return{
          yourtask:'',  
         currenttasks:[]
         };
      
     },
     methods:{
         getcurentasks:function(){
          currenttasks=localStorage.getItem("my");
          currenttasks = currenttasks ? JSON.parse(currenttasks) : [];
          return currenttasks;
         
         }
         mytasks:function(){
         let currenttasks=getcurentasks();
  
         } 
         
         
     }
 }
 </script>  