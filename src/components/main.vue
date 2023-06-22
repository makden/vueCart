<template>
  <div class="catalog" v-for="product in products">
    {{ product.title }}
  </div>
</template>

<script>
import axios from "axios";
console.log("ddd");
export default {
  name: 'main',
  props: {
    msg: String,
  },
  data() {
    return {
      products: this.getProducts(),
    };
  },
   watch: {
    getProducts();
    },
  methods: {
    getProducts() {
      axios
        .get('https://jsonplaceholder.typicode.com/posts')
        .then((response) => {
           this.products = response;
          console.log(response);
        })
        .catch((error) => {
          alert('Ошибка! Нет доступа к API. ' + error);
        });
    }
  },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
