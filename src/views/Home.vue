<template>
  <div class="home">
    <h1>Drum Sets</h1>
    <div v-for="product in products" v-bind:key="product.id">
      <h2>{{ product.name }}</h2>
      <h2>{{ product.price }}</h2>
      <img v-bind:src="product.images" alt="" style="width: 50%" />
      <h2>{{ product.description }}</h2>
    </div>
  </div>
</template>

<style></style>

<script>
/* global axios */
export default {
  data: function () {
    return {
      products: [],
    };
  },
  created: function () {
    this.indexProducts();
  },
  methods: {
    indexProducts: function () {
      axios.get("/products").then((response) => {
        this.products = response.data;
        console.log("All products", this.products);
      });
    },
  },
};
</script>
