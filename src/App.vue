<template>
  <div>
    <h1>counter : {{count}}</h1>
    <button @click="inc(1)">Increment</button>
    <button @click="dec(1)">Decrement</button>
    <Child :count="count" :incfn="inc" :decfn="dec"></Child>
  </div>
</template>

<script>
import Child from './child1';
export default {
  components: {
    Child : Child
  },
  data:function(){
    return{
      count : 0
    }
  },
  methods:{
    inc(x){
      this.count += x;
    },
    dec(x){
      this.count -= x;
    }
  }
}
</script>

<style scoped>

</style>