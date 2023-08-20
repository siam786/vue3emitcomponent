<script setup>
import Header from './assets/components/Header.vue';
import Footer from './assets/components/Footer.vue';
import ParentComponent from './assets/components/ParentComponent.vue';
</script>

<template >
  <Header/>
  <div class="flex items-center justify-center h-screen bg-gray-900">
    <ParentComponent/>
  </div>
<Footer/>
</template>

