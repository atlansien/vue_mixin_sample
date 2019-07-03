<template>
  <div>
    <ul>
      <li v-for="number in numbers">{{ number }}</li>
    </ul>
  </div>
</template>

<script>
import { mixin } from "./mixin";
export default {
  mixins: [mixin],
};
</script>
