<script setup lang="ts">
interface CardProps {
  name: string;
  img: string;
  text: string;
}

const props = defineProps<CardProps>();
</script>

<template>
  <div class="card">
    <img class="card-img-top" :src="img" alt="Card image cap" />
    <div class="card-body">
      <h5 class="card-title">{{ name }}</h5>
      <p class="card-text text-truncate">
        {{ text }}
      </p>
      <a :href="`/restaurants/${name}`" class="btn btn-primary"
        >Read about {{ name }}</a
      >
    </div>
  </div>
</template>
