<template>
    <div class="bg-white shadow-md rounded-lg p-6 m-4">
      <h2 class="text-2xl font-bold mb-4">{{ title }}</h2>
      <ul class="list-disc pl-5">
        <li v-for="(item, index) in items" :key="index" class="mb-2">
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