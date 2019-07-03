<template>
  <div class="container">
    <h1>mixin sample</h1>
    <hr>
    <h2>App.vueで読み込んだmixin</h2>
    <button @click="pushNumberInNumbersArr">Add number</button>
    <ul>
      <li v-for="number in numbers">{{ number }}</li>
    </ul>
    <hr>
    <h2>別コンポーネント(List.vue)で読み込んだmixin</h2>
    <app-list></app-list>
  </div>
</template>

<script>
import { mixin } from "./mixin";
import List from "./List.vue";
export default {
  mixins: [mixin],
  methods: {
    pushNumberInNumbersArr() {
      const number = Math.floor(Math.random() * this.numbers.length);
      this.numbers.push(number);
    }
  },
  components: {
    appList : List,
  }
}
</script>

<style>

</style>
