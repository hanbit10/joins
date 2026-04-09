<script lang="ts" setup>
import { useRouter } from 'vue-router'

const router = useRouter()

function privacyPolicy() {
  router.push('/privacy-policy')
}

function legalNotice(){
  router.push('/legal-notice')
}
</script>

<template>
  <button @click="legalNotice">Legal Notice</button>
  <button @click="privacyPolicy">Privacy Policy</button>
</template>
