<script setup lang="ts">
import { ref } from 'vue'

const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2,
  },
}
</script>

<template>
  <div class="w-60 relative mt-6">
    <div class="relative w-40 h-40">
      <img
        v-motion
        :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
        :enter="final"
        class="absolute top-0 left-0 right-0 bottom-0"
        src="https://sli.dev/logo-square.png"
      />
      <img
        v-motion
        :initial="{ y: 500, x: -100, scale: 2 }"
        :enter="final"
        class="absolute top-0 left-0 right-0 bottom-0"
        src="https://sli.dev/logo-circle.png"
      />
      <img
        v-motion
        :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
        :enter="final"
        class="absolute top-0 left-0 right-0 bottom-0"
        src="https://sli.dev/logo-triangle.png"
      />
    </div>

    <div
      class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
      v-motion
      :initial="{ x: -80, opacity: 0 }"
      :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }"
    >
      Slidev
    </div>
  </div>
</template>
