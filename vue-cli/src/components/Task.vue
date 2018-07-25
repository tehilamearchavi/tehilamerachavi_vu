
<template>
<div>
<from>
<input type="data" v-model="task.time" >
<input type="text" v-model="task.content">
<button @click="keepme"></button>
<from>
</div>
</templae>
<script>
export default{

data(){
return{
    
task:{
time:data,
content:''
}
};
},
methods:{
    keepme:function(){
         let mytaskprev=localStorage.getItem("my");
         mytaskprev=mytaskprev ? JSON.parse(mytaskprev) : [];
         mytaskprev.push(this.task);
         localStorage.setItem("my", JSON.stringify(mytaskprev));
    }
}

}

</script>