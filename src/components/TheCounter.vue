<template>
  <div>
    <h3>TheCounter</h3>
    <slot :message="count" name="default">
      <p>Count: {{ count }}</p>
    </slot>
    <button @click="click">Click me</button>
  </div>
</template>

<script setup lang="ts">
  import { defineExpose } from "vue";
  import { counter as count } from '../store.js'

  const click = () => {
    count.value++
  }

  defineExpose({
    click,
  })

</script>
