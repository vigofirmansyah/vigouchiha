<script setup lang="ts">
// const { data: products } = await useFetch("https://fakestoreapi.com/products");
// const data = await useFetch("https://fakestoreapi.com/products");
const { data, status, error, refresh, clear } = await useFetch(
  "https://carapi.app/api/years/powersports",
);
var products: any = data.value;
console.log(data.value);
</script>
<template>
  <div>
    <h2>TESSTTT</h2>
    <h3>Competition Auto M x Drive</h3>
    <h4>$202,500</h4>
    <img src="/NFSUB_Garage_McLaren_F11993.webp" alt="BWM M4 GTS" />
  </div>

  <div v-for="p in products">
    <h1>{{ p.title }}</h1>
  </div>
</template>
