<script setup lang="ts"> 
   async function api() {
    const apiBun = await useFetch('/home', {
      method: 'GET',
      baseURL: "http://localhost:3333/"
    });

    let text = JSON.stringify(apiBun.data.value);
    text = JSON.parse(text).data;
    
    console.log(text);
 }
</script>

<template>
  <div class="flex flex-wrap justify-center align-middle">
    <button class="btn" @click="api">clique aqui</button>
  </div>
</template>
