<template>
  <div class="container bg-indigo-200 min-h-screen m-auto pt-40">
    <div class="m-auto w-56 flex flex-col justify-center text-center p-4 mb-10">
      <switch-a v-model:switch-a="switchA" />
      <span class="mt-4 p-2 text-white rounded"
        :class="{'bg-red-800': !switchA, 'bg-green-800': switchA}"
      >{{ switchA ? 'On' : 'Off' }}</span>
    </div>
    <div class="m-auto w-56 flex flex-col justify-center text-center p-4">
      <switch-b v-model:switch-b="switchB" />
      <span class="mt-4 p-2 text-white rounded"
        :class="{'bg-red-800': !switchB, 'bg-green-800': switchB}"
      >{{ switchB ? 'On' : 'Off' }}</span>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import SwitchA from './components/SwitchA.vue'
import SwitchB from './components/SwitchB.vue'
export default {
   components: {
     SwitchA,
     SwitchB
   },
   setup () {
     // DATA
     const switchA = ref(false)
     const switchB = ref(false)

     return { switchA, switchB }
   }
}
</script>

<style>

</style>
