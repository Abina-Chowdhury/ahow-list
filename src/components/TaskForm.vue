<script setup>
import { ref } from 'vue';

  defineProps(["name","time"]);

</script>
<!-- TaskForm.vue -->
<template>
    <div>
      <input 
      :value="name" @input="$emit('update:name',$event.target.value)"
/>
      <input v-model="tasks.name" label="Name"/>
      <input v-model="tasks.time" label="Time"/>
      
      <button @click="submitForm">Submit</button>
    </div>
  </template>
  

  