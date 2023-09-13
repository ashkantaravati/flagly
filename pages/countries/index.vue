<template>
  <div>
    <div class="bg-white rounded-lg p-3 space-x-4 flex">
      <FDropdown placeholder="Continent" v-model="selectedContinent"
        >O</FDropdown
      >
      <FDropdown placeholder="Name" v-model="selectedContinent">O</FDropdown>
    </div>

    <div class="bg-white rounded-lg px-5 py-7 my-8">
      <h2 class="text-xl">
        Every Country in {{ selectedContinent }} named {{ nameQuery }}
      </h2>
      <FFlagCard
      class="flex flex-col"
        v-for="country in countries"
        :country="country"
        :key="country.id"
      />
    </div>
  </div>
</template>

<script setup>
const selectedContinent = ref("America");
const nameQuery = ref("asf");
const countries = ref([
  {
    id: 1,
    name: "Germany",
    continent: "Europe",
    flag: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Flag_of_Iran.svg/630px-Flag_of_Iran.svg.png?20140922081832",
  },
  {
    id: 3,
    name: "Germany",
    continent: "Europe",
    flag: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Flag_of_Iran.svg/630px-Flag_of_Iran.svg.png?20140922081832",
  },
  {
    id: 4,
    name: "Germany",
    continent: "Europe",
    flag: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Flag_of_Iran.svg/630px-Flag_of_Iran.svg.png?20140922081832",
  },
  {
    id: 2,
    name: "Germany",
    continent: "Europe",
    flag: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Flag_of_Iran.svg/630px-Flag_of_Iran.svg.png?20140922081832",
  },
]);
</script>

<style scoped></style>
