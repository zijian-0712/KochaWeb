<script setup>
import {reactive, ref} from "vue";

let a=ref({num:1})
function click(){
  a.value.num++;
}
</script>

<template>
<button v-on:click="click">{{a.num}}</button>
</template>

<style scoped>

</style>