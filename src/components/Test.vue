<script setup>
import {reactive, ref} from "vue";

let a=ref({
  name:"name",
  count:0
})
function click(){
a.value.count++
}
</script>

<template>
  <p>  {{a.name}}</p>
<button v-on:click="click">{{a.count}}</button>
</template>

<style scoped>

</style>