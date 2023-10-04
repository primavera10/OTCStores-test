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
  import { ref, defineExpose } from "vue";

  const count = ref(0)
  const click = () => {
    count.value++
  }

  defineExpose({
    click,
  })

</script>
