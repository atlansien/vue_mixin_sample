<template>
  <div>
    <ul>
      <li v-for="(number, i) in numbers" :key="i">{{ number }}</li>
    </ul>
  </div>
</template>

<script>
import { mixin } from './mixin'
export default {
  mixins: [mixin]
}
</script>
