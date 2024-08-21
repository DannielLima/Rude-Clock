<template>
    <div class="flex items-center justify-center h-screen bg-gray-100">
      <div class="text-center">
        <h1 class="text-3xl font-bold mb-4">Que horas são?</h1>
        <button
          @click="showMessage"
          class="px-6 py-3 bg-blue-500 text-white font-semibold rounded-md shadow-md hover:bg-blue-600 transition duration-300"
        >
          Me diga
        </button>
        <p v-if="message" class="mt-4 text-xl text-red-500">{{ message }}</p>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent, ref } from 'vue';
  
  export default defineComponent({
    setup() {
      const message = ref('');
  
      const showMessage = () => {
        message.value = 'Olhe para o seu relógio, babaca.';
      };
  
      return {
        message,
        showMessage
      };
    }
  });
  </script>
  
  <style scoped>
  body {
    font-family: 'Inter', sans-serif;
  }
  </style>
  