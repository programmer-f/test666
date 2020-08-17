<template>
  <div class="box">
        <div v-for="(person,index) in newPersons" :key="index">
          <p>{{person.name}}</p>
          <p>{{person.age}}</p>
        </div>
  </div>
</template>


<script>
  export default {
      name:'App',
      data(){
        return{
            persons:[
              {name:'Ted',age:5},
              {name:'Lisa',age:8},
              {name:'Andy',age:11},
              {name:'Peter',age:15},
              {name:'Andrew',age:24},
              {name:'Rose',age:30},
              {name:'Violet',age:25},
              {name:'Joe',age:17},
              {name:'Mike',age:19},
              {name:'Tee',age:22},
              {name:'Dick',age:25},
              {name:'Alex',age:28},
              {name:'Frank',age:25},
              {name:'CoCo',age:32},
              {name:'TS',age:21},
              {name:'Pink',age:25},
              {name:'Justin',age:25}
            ],

        }
      },
    computed:{
        newPersons(){
          return this.persons.filter(function (value,index) {
            return value.age >= 20;
          });
        }
    }
  }
</script>


<style scoped lang="scss">
  *{
    margin: 0;
    padding: 0;
  }
  .box{
    display: flex;
    flex-wrap: wrap;

    div{
      width: 100px;
      height: 100px;
      border: 1px solid #000;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  }
</style>
