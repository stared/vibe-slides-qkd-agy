<script setup lang="ts">
const props = defineProps<{
  name: string
  role: string
  image: string
  color: string
}>()

const base = import.meta.env.BASE_URL || '/'
const imageSrc = props.image.startsWith('/') ? base.replace(/\/$/, '') + props.image : props.image
</script>

<template>
  <div class="flex flex-col items-center">
    <img
      :src="imageSrc"
      class="h-48 rounded-full border-4 shadow-lg mb-4"
      :class="`border-${color}-500`"
    />
    <h3 class="font-bold" :class="`text-${color}-400`">{{ name }}</h3>
    <p class="text-sm opacity-80">{{ role }}</p>
  </div>
</template>
