<script setup lang="ts">
import { onMounted, ref } from 'vue'
import Button from './components/Button/Button.vue'
const buttonRef = ref()
onMounted(() => {
  console.log(buttonRef.value)
})
</script>



<template>
  <Button type="success" size="large" round plain nativeType="submit" ref="buttonRef">按钮</Button>
</template>
