<script setup>
import {ref, onMounted, onBeforeMount, onUnmounted, onUpdated, nextTick, onBeforeUnmount } from 'vue';


const items = ref ([
  'https://images.unsplash.com/photo-1682685797507-d44d838b0ac7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80',
  'https://images.unsplash.com/photo-1691633324809-f744d11d2dfb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80',
  'https://images.unsplash.com/photo-1682687982185-531d09ec56fc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80',
  'https://images.unsplash.com/photo-1691394790591-b1ce2093b045?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80'
])

onMounted(()=>{
  carousel = new Flickity('.carousel', {})
});


onBeforeUnmount(()=>{
  carousel.destroy()
});


</script>

<template>

  <div class="carousel">
    <div class="item" v-for="(item, index) in items" :key="index">
      <img :src="item" alt="">
    </div>
  </div>

</template>

<style scoped>

</style>
