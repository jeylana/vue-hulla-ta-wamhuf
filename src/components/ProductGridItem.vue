<template>
  <div class="product-grid-item">
    <img class="product-image" :src="product.image" />
    <div class="product-description">
      <h2 class="product-name">{{ product.name }}</h2>
      <p>£{{ product.price }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductGridItem',
  props: {
    product: { type: Object, required: true, default: () => ({}) },
  },
};
</script>

<style scoped>
.product-grid-item {
  background: #ddebe8;
  max-width: 150px;
  display: flex;
  margin-bottom: 20px;
}

.product-description {
  display: flex;
  flex-direction: column;
  align-items: start;
}

.product-image {
  width: 100%;
}
</style>
