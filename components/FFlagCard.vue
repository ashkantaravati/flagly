<template>
  <div class="flex  w-1/4 mx-2 my-3">
    <div class="border-l-8 border-solid">
        <img class="rounded-r-lg" :src="country.flag" alt="" />

    </div>
    <div>
      <span class="text-lg font-semibold">
        {{ country.name }}
      </span>
      <span>
        {{ country.continent }}
      </span>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["country"])
</script>

<style lang="scss" scoped></style>
