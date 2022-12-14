<script setup>
import { ref } from 'vue'

const lang = ref('Welcome');
const trans = ref('EN >> ID');

function toggleLang(){
  [lang.value, trans.value] = lang.value === 'Welcome' ? ["Selamat datang", "ID >> EN"] : ["Welcome", 'EN >> ID']
}
</script>

<template>
<div class="container">
  <h1>{{lang}}</h1>
  <button @click="toggleLang" >{{trans}}</button>
</div>
</template>

<style>
.container {
  width: 50%;
  margin: 0 auto;
  text-align: center;
}
</style>
