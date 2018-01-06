<template>
  <div class="todo-header">
    <div class="overlay"></div>
    <time class="clearfix">
      <span class="day">{{ date }}</span>
      <span class="dayofweek">{{ weekDay }}</span>
      <span class="month">{{ month }}, {{ year }}</span>
    </time>
    <div class="add-circle" @click="add">
      <i class="fa fa-plus"></i>
    </div>
</div>

</template>


<script>

const month = ["January", "February", "Mach", "April", "May", "June", "July", "August", "September", "October", "November", "September"],
    weekday = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
export default {
  
    data(){
      return{
         data: '',
         weekDay: '',
         month: '',
         year: '',
      }
    },
    
    beforeCreate(){

    },
    created(){
      const d = new Date();
      this.date = d.getDate();
      this.weekDay = weekday[d.getDay()];
      this.month =  weekday[d.getMonth()];
      this.year = d.getFullYear();
    },
    // 生命周期就是些钩子函数， 在特定的事件发生
    beforeMounted(){
        
    },
    mounted(){

    },
    methods : {
      add(){
        console.log('add');
      }
    }
}
</script>


<style>

</style>

