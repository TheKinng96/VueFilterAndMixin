<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <h1>Filters & Mixins</h1>
        <p>{{ text | toUppercase | to-lowercase }}</p>
        <hr />
        <input type="text" v-model="filterText" />
        <hr />
        <ul>
          <li v-for="fruit in filteredFruits" :key="fruit.index">{{fruit}}</li>
        </ul>
        <hr />
        <app-list></app-list>
      </div>
    </div>
  </div>
</template>

<script>
import List from "./List.vue";
import { fruitsMixin } from "./fruitsMixin";

export default {
  data() {
    return {
      text: "HI Random text",
    };
  },
  filters: {
    toUppercase(value) {
      return value.toUpperCase();
    },
  },
  mixins: [fruitsMixin],
  components: {
    appList: List,
  },
};
</script>

<style>
</style>
