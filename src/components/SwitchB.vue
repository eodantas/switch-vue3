<template>
  <div class="flex items-center justify-center w-full">
    <label for="toggleB" class="flex items-center cursor-pointer">
      <!-- toggle -->
      <div class="relative">
        <!-- input -->
        <input type="checkbox" id="toggleB" class="sr-only" :checked="switchB" @change="$emit('update:switchB', $event.target.checked)" />
        <!-- line -->
        <div class="block bg-gray-600 w-14 h-8 rounded-full"></div>
        <!-- dot -->
        <div class="dot absolute left-1 top-1 bg-white w-6 h-6 rounded-full transition"></div>
      </div>
    </label>
  </div>
</template>

<script>
export default {
  props: { switchB: { type: Boolean, default: false } },
  emits: ['update:switchB']
}
</script>

<style scoped>
input:checked ~ .dot {
  transform: translateX(100%);
  background-color: #48bb78;
}
</style>
