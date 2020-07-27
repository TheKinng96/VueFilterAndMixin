<template>
  <div>
    <h1>Filters & Mixins</h1>
    <input type="text" v-model="filterText" />
    <ul>
      <li v-for="fruit in filteredFruits" :key="fruit.index">{{fruit}}</li>
    </ul>
  </div>
</template>

<script>
import { fruitsMixin } from "./fruitsMixin";
export default {
  mixins: [fruitsMixin],
};
</script>

<style>
</style>
