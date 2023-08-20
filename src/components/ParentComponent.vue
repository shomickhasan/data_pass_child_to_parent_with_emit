<script setup>
import ChildComponent from "@/components/ChildComponent.vue";
import {ref} from "vue";
const message = ref('Hello from Parent!');
const ChildMessage= (msg)=>{
  message.value= msg

}


</script>

<template>
  <div class="container p-4">
    <h1 class="text-xl font-bold mb-4">Parent Component</h1>
   <ChildComponent :message="message" @ChildMessage="ChildMessage"/>
  </div>
</template>

<style scoped>

</style>