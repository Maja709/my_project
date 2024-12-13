<script setup>
import { ref } from 'vue';
import { my_project_backend } from 'declarations/my_project_backend/index';
let greeting = ref('');

const getDataFromNBP = async ()=>{
  const res = await fetch("api.nbp.pl/api/exchangerates/tables/A/?format=json")
  const jsonData = res.json()
  console.log(jsonData)
  const rates = jsonData(0).rates
}
getDataFromNBP()
</script>

<template>
  <main>
    <img src="/logo2.svg" alt="DFINITY logo" />
    <br />
    <br />
  </main>
</template>
