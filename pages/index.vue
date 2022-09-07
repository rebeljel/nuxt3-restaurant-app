<script setup lang="ts">
import restaurants from "@/data.json";
const { isDarkMode } = useDarkMode();
</script>

<template>
  <div>
    <div class="container">
      <h1>Welcome to Restaurantly</h1>
      <NuxtLink to="/restaurants">Restaurants</NuxtLink>
      <div class="row">
        <div v-for="r in restaurants" class="col-sm-4 mt-5 mb-5">
          <RestaurantCard :name="r.name" :img="r.imageUrl" :text="r.content" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  text-align: center;
  margin-top: 5rem;
}
</style>
