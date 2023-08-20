<template>
  <div
    class="max-w-lg p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
  >
    <h1 class="p-4 text-4xl font-bold text-left text-white rounded-lg">
      Child Component
    </h1>
    <p class="p-4 text-lg text-white">{{ msg }}</p>
    <button
      class="px-4 py-2 font-bold text-white bg-blue-500 rounded hover:bg-blue-700"
      @click="
        $emit('childMsg', `Hello from Child Component & data from ${msg}`)
      "
    >
      show message
    </button>
  </div>
</template>

<script setup>
import { defineEmits, defineProps } from "vue";
defineProps(["msg"]);
defineEmits(["childMsg"]);

</script>
