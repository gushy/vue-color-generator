<template>
  <div class="flex flex-col items-center justify-center h-screen bg-gray-100">
    <div
      class="w-64 h-64 rounded shadow-lg mb-6"
      :style="{ backgroundColor: color }"
    ></div>
    <p class="text-lg font-mono mb-4">{{ color }}</p>
    <button
      class="px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 transition"
      @click="generateColor"
    >
      Generate Color
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const color = ref('#3498db')

const generateColor = () => {
  const randomColor = `#${Math.floor(Math.random() * 16777215).toString(16)}`
  color.value = randomColor
}
</script>