<template>
  <div>
    <div v-if="((size - 1) > 0)">
      <ChristmasTree :size="(size - 1)" />
    </div>
    <div class="flex flex-row justify-center">
      <div
        v-for="number in size" :id="`${number}`"
        class="relative rounded-full bg-green w-16 h-16 -m-2 flex justify-center items-center" />
    </div>
  </div>
</template>

<script setup lang="ts">
import ChristmasTree from './ChristmasTree.vue'

withDefaults(
  defineProps<{
    size: number
  }>(),
  {
    size: 1,
  }
)
</script>
