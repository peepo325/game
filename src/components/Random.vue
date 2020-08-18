<template>
  <div>

    <button @click="picker">Random</button>
    <H1>{{chosenPlayer}}</H1>
  
  </div>
</template>

<script>
export default {
  name:'Random',
  data: function() {
    return{
      data:{
        Player:[
        {name:'Doraemon',hp:100,image:''},
        {name:'Pickachu',hp:100,image:''},
        {name:'Scooby-doo',hp:100,image:''},
        ],chosenPlayer:'',
        Monster:[
          {name:'Jai-ant',hp:100,image:''},
          {name:'Ghost',hp:100,image:''},
          {name:'Kai-Ju',hp:100,image:''},
        ],
  }
}
  },
  methods:{
    picker:function(){
      var chosenPlayer = Math.floor(Math.random() * this.list.length);
      this.chosenPlayer = this.list[chosenPlayer];
    }
  }
}
   

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>