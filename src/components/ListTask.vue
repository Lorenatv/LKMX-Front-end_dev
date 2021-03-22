<template>
  <div class="list">
    <div v-for="task in tasks" :key="task.id">
        <ItemsTask :task="task"/>
    </div>
    <div v-if="tasks.length == 0">
        <h2>No has agregado tareas</h2>
    </div>
  </div>
</template>

<script>
import ItemsTask from "@/components/ItemsTask";
import {mapGetters} from "vuex";

export default {
  components:{
    ItemsTask
  },
  computed:{
    ...mapGetters(["tasks"])
  }
};
</script>


<style>
h1 {
    text-align: left;
    font: 15px "Poppins", sans-serif;
    font-weight: bold;
    font-size: 32px;
}
h2 {
    text-align: left;
    font: 20px "Poppins", sans-serif;
    font-weight: bold;
    color:#89898b
}
h3 {
    text-align: left;
    font: 16px "Poppins", sans-serif;
    font-weight: bold;
    margin-top: 5px;
}
h3::before{
    background: url("../assets/icons/rec.svg") no-repeat;
    background-size: 20px 20px;
    display: inline-block;
    width: 10px;
    height: 5px;
    content: "";
    margin-right: 15px;
    background-size: 10px 20px;
}
body{
    background: #f1f2f7;
}
.container{
    max-width: 650px;
    background: #fff;
    border-radius: 20px;
    padding: 15px;
    box-shadow: 0px 5px 5px 0px rgba(0, 0, 0, 0.1);
}
.list{
    margin-top: 10px;
    background: #f1f2f7;
    border-radius: 15px;
    padding: 15px;
    padding-top: 20px;
    word-wrap: break-word;
}
.row{
    margin: auto;
}
.task{
    white-space: nowrap;
    overflow: hidden;
}
input[type="text"]{
    font: 16px "Poppins", sans-serif;
    padding: 10px;
    background: #ffffff;
    color: black;
    border: 2px solid #b9c0c6;
    border-radius: 10px;
    transition: border 0.3s linear;
}
input[type="text"]:focus{
    outline: none;
    border: 2px solid #f8bfcc;
    box-shadow: none !important;
}
.btn.add{
    font: 16px "Poppins", sans-serif;
    color:#fff;
    background-color: #1146a0;
    border-radius: 10px;
    box-shadow: none !important;
}
.btn.add:hover{
    background-color: #1a4ca1;
}
.btn.edit{
    background: url("../assets/icons/edit.svg") no-repeat;
    background-size: 20px 20px;
    background-position: center;
    font: 16px "Poppins", sans-serif;
    color:#fff;
    background-color: #3370d7;
    border-radius: 10px;
    box-shadow: none !important;
    width: 50px;
    height: 38px;
    
}
.btn.edit:hover{
    background-color: #16b8a2;
    border: 2px solid #054441;
}
.btn.save{
    background: url("../assets/icons/diskette.svg") no-repeat;
    background-size: 20px 20px;
    background-position: center;
    font: 16px "Poppins", sans-serif;
    color:#fff;
    background-color: #3370d7;
    border-radius: 10px;
    box-shadow: none !important;
    width: 50px;
    height: 38px;
}
.btn.save:hover{
    background-color: #52df59;
    border: 2px solid #227203;
}
.btn.delete{
    background: url("../assets/icons/trash.svg") no-repeat;
   background-size: 20px 20px;
   background-position: center;
    font: 16px "Poppins", sans-serif;
    color:#fff;
    background-color: #3370d7;
    border-radius: 10px;
    box-shadow: none !important;
    width: 50px;
    height: 38px;
}
.btn.delete:hover{
    background-color: #ec513c;
    border: 2px solid #740505;
}
</style>
