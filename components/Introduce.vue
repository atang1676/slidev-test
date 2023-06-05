<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  count: {
    default: 0,
  },
})

const counter = ref(props.count)
</script>

<template>
  <div class="page-title"></div>
</template>

<style lang="scss" scoped>
.page-title {
}
</style>
