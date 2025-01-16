<template>
  <div class="min-h-screen bg-black text-white">
    <!-- Hero Section -->
    <header class="relative h-screen">
      <div class="absolute inset-0 bg-gradient-to-b from-black/70 to-black/30 z-10"></div>
      <div class="absolute inset-0 flex flex-col justify-center  px-8 z-20">
        <Jumbotron />
      </div>
      <div class="absolute inset-0 z-0">
        <img
          src="https://images.unsplash.com/photo-1509440159596-0249088772ff?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1920&q=80"
          alt="Artisan bread" class="w-full h-full object-cover" />
      </div>
    </header>

    <!-- Detalles del producto -->
    <section class="py-16 px-8 bg-black">
      <div class="flex justify-around">
        <div class="flex items-center gap-4">
          <img src="assets/icon_clock.svg" alt="reloj">
          <h1 class="font-bold">Fermentado por 24 horas</h1>
        </div>
        <div>
          <div class="flex items-center gap-4">
            <img src="assets/icon_clock.svg" alt="reloj">
            <h1 class="font-bold">Fermentado por 24 horas</h1>
          </div>
        </div>
        <div>
          <div class="flex items-center gap-4">
            <img src="assets/icon_clock.svg" alt="reloj">
            <h1 class="font-bold">Fermentado por 24 horas</h1>
          </div>
        </div>
      </div>
    </section>

    <!-- Products Section -->
    <section class="py-16 px-8 bg-zinc-900">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-3xl font-bold mb-12 text-center text-amber-500">CUSTOMER FAVOURITES</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <!-- Product Cards -->
          <ProductCard v-for="product in products" :key="product.name" :product="product" />
        </div>
      </div>
    </section>

  </div>
</template>

<script setup>


const products = [
  {
    name: 'Whole Spelt',
    description: 'Traditional spelt bread',
    price: 6.50,
    image: 'https://images.unsplash.com/photo-1586444248902-2f64eddc13df?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80'
  },
  {
    name: 'Six Rye Multigrain',
    description: 'Hearty multigrain bread',
    price: 7.00,
    image: 'https://images.unsplash.com/photo-1509440159596-0249088772ff?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80'
  },
  {
    name: 'Stone Ground Wheat',
    description: 'Classic wheat bread',
    price: 5.50,
    image: 'https://images.unsplash.com/photo-1555951015-6da899b5c2cd?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80'
  },
  {
    name: 'Bagel Bundle',
    description: 'Fresh daily bagels',
    price: 8.00,
    image: 'https://images.unsplash.com/photo-1585478259715-876acc5be8eb?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80'
  }
]
</script>