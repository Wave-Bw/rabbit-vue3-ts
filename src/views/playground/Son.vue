<script lang="ts" setup>
const emit = defineEmits(['update'])
</script>

<template>
  <h3 @click="emit('update', 100)">子组件</h3>
</template>

<style scoped lang="less"></style>
