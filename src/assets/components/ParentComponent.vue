<template>
  <div
    class="max-w-lg p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
  >
    <h1 class="p-4 text-4xl font-bold text-left text-white rounded-lg">
      Parent Component
    </h1>
    <p class="p-4 text-lg text-white">
      {{
        emitMessage == false
          ? "Parent Component Message:"
          : "Child Component Message:"
      }}
      <span class="font-bold text-red-400">
        {{ emitMessage == false ? parentMessage : emitMessage }}
      </span>
    </p>
  </div>
  <div class="p-4">
    <ChildComponent :msg="parentMessage" @childMsg="handleMsg" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";
const parentMessage = ref("Parent Component");
const emitMessage = ref("");
const handleMsg = (msg) => {
  emitMessage.value = msg;
};
</script>
