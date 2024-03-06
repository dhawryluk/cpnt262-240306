<script setup>
import { computed } from "vue";
const players = [
  {
    name: "Smizzy",
    gun: "SVA 545",
    kd: 3.2,
  },
  {
    name: "Hamlet",
    gun: "KAT",
    kd: 2.4,
  },
  {
    name: "Scgeeezy",
    gun: "Ram9",
    kd: 1.6,
  },
  {
    name: "Modded",
    gun: "Bruen MK9",
    kd: 0.8,
  },
];

const filteredPlayers = computed(() => {
  return players.filter((item) => item.kd > 2);
});
</script>

<template class="">
  <main class="">
    <header class="my-8">
      <h1
        class="bg-gray-800 text-5xl text-orange-500 shadow-2xl text-center w-full p-4"
      >
        Modern Warfare III
      </h1>
      <h3 class="text-center text-3xl mt-5 text-orange-800">
        {{ filteredPlayers }}
      </h3>
    </header>
  </main>
</template>
