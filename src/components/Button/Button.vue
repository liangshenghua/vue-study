<!--  -->
<template>
  <button
    class="ms-button"
    ref="_refEle"
    :class="{
      [`ms-button-${type}`]: type,
      [`ms-size-${size}`]: size,
      'is-plain': plain,
      'is-round': round,
      'is-circle': circle,
      'is-disabeld': disabled,
    }"
    :disabled="disabled"
    :type="nativeType"
  >
    <slot></slot>
  </button>
</template>

<script setup lang='ts'>
import { onMounted, ref } from 'vue'
import { ButtonProps } from './types'
const { nativeType = 'button' } = defineProps<ButtonProps>()
defineOptions({ name: 'MsButton' })

const _refEle = ref<HTMLButtonElement>()
onMounted(() => {
  console.log(_refEle.value)
})

defineExpose({
  refEle: _refEle,
})
</script>

<style  scoped>
</style>
