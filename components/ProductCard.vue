<template>
  <div class="bg-zinc-800 rounded-lg overflow-hidden group hover:bg-zinc-700 transition">
    <div class="relative pt-[100%]">
      <img :src="product.image" :alt="product.name" 
           class="absolute inset-0 w-full h-full object-cover" />
    </div>
    <div class="p-4">
      <h3 class="text-lg font-semibold">{{ product.name }}</h3>
      <p class="text-zinc-400">{{ product.description }}</p>
      <div class="mt-4 flex justify-between items-center">
        <span class="text-amber-500">${{ product.price.toFixed(2) }}</span>
        <button class="bg-amber-700 px-4 py-2 rounded hover:bg-amber-600 transition">
          Add
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>
