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
export default {
  data: function () {
    return {
      products: [
        {
          id: 1,
          name: "DW Design Series",
          description: "A nice drum set.",
          price: 500,
          images:
            "https://images.reverb.com/image/upload/s--V5KFpzg_--/f_auto,t_supersize/v1587860801/jiryixflpenossdgn9jk.jpg",
        },
        {
          id: 2,
          name: "TAMA Studio Series",
          description: "A very nice drum set.",
          price: 900,
          images:
            "https://images.reverb.com/image/upload/s--yOXCdryk--/f_auto,t_supersize/v1587861247/fcxw6tknq0p8ryzcket9.jpg",
        },
      ],
    };
  },
  created: function () {},
  methods: {},
};
</script>
