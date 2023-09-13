<template>
  <div class="bg-slate-100 rounded-lg p-2 w-1/4 flex">
    <div class="w-8 border-r-2 border-gray"><slot /></div>
    <div class="ms-3 grow">
      <div class="text-xs text-gray-300">{{ placeholder }}</div>
      <div>{{ modelValue }}</div>
    </div>
    <button class="w-8">^</button>
  </div>
</template>

<script setup>
const props = defineProps(["modelValue", "placeholder"]);
</script>

<style lang="scss" scoped></style>
