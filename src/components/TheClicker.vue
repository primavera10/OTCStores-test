<template>
  <div>
    <h3>TheClicker</h3>
    <button @click="$emit('addCount')">Click me too</button>
  </div>
</template>

<script setup lang="ts">
  import {defineEmits} from 'vue'
  defineEmits(['addCount'])
</script>
