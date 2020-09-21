<template>
  <div>
    <app-stock v-for="(stock, id) in stocks" :key="id" :stock="stock"></app-stock>
  </div>
</template>

<script>
import stock from './Stock.vue';

  export default {
      components: {
          appStock: stock
      },
      computed: {
        stocks(){
          return this.$store.getters.stocks;
        }
      }
  }

</script>
