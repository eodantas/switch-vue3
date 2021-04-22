<template>
  <div class="flex items-center justify-center w-full">
    <label for="toogleA" class="flex items-center cursor-pointer">
      <!-- toggle -->
      <div class="relative">
        <!-- input -->
        <input id="toogleA" type="checkbox" class="sr-only" :checked="switchA" @change="$emit('update:switchA', $event.target.checked)" />
        <!-- line -->
        <div class="w-10 h-4 bg-gray-400 rounded-full shadow-inner"></div>
        <!-- dot -->
        <div class="dot absolute w-6 h-6 bg-white rounded-full shadow -left-1 -top-1 transition"></div>
      </div>
    </label>
  </div>
</template>

<script>
export default {
  props: { switchA: { type: Boolean, default: false } },
  emits: ['update:switchA']
}
</script>

<style scoped>
input:checked ~ .dot {
  transform: translateX(100%);
  background-color: #48bb78;
}
</style>
