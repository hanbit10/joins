<script lang="ts" setup>
import { useRouter } from 'vue-router';

const router = useRouter()

function home(){
  router.push('/')
}

</script>

<template>
  <button @click="home">home</button>
  <h1>hello</h1>
</template>
