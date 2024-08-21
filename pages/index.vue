<template>
    <div class="flex items-center justify-center min-h-screen bg-gray-100">
      <div class="text-center p-8 bg-white shadow-lg rounded-lg max-w-sm w-full">
        <h1 class="text-4xl font-bold mb-6 text-gray-800">
          Que horas são?
        </h1>
        <button
          @click="showMessage"
          class="px-6 py-3 bg-blue-500 text-white font-semibold rounded-lg shadow-lg transition-transform duration-300 hover:bg-blue-600 hover:scale-105 active:bg-blue-700"
        >
          Me diga
        </button>
        <p v-if="message" class="mt-6 text-xl text-red-600">
          {{ message }}
        </p>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent, ref } from 'vue';
  
  export default defineComponent({
    setup() {
      const message = ref('');
  
      const showMessage = () => {
        message.value = 'Olhe no seu relógio, babaca.';
      };
  
      return {
        message,
        showMessage
      };
    }
  });
  </script>
  
  <style scoped>
  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
  }
  </style>
  