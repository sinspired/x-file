<template>
  <div class="bg-white shadow-xl rounded-lg overflow-hidden transition duration-300 hover:shadow-2xl m-4">
    <div class="bg-blue-500 text-white p-4">
      <h2 class="text-2xl font-bold">{{ title }}</h2>
    </div>
    <ul class="p-6">
      <li v-for="(item, index) in items" :key="index" class="mb-3 flex items-start">
        <svg class="w-5 h-5 text-blue-500 mr-2 mt-1 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
        </svg>
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  title: String,
  items: Array
})
</script>