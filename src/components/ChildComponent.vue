<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  message: String,
});

defineEmits(['ChildMessage'])


</script>

<template>
  <div class="container p-4 border rounded">
    <h2 class="text-lg font-semibold mb-2">Child Component</h2>
    <p class="mb-2">{{ props.message }}</p>
    <button @click="$emit('ChildMessage','Hi this is message form child!!')" class="btn btn-primary">Emit Message</button>
  </div>
</template>

<style scoped>

</style>