<template lang="pug">
  .container
    .gridhead hellooooooooooooooo
    .div(v-for="key in keys")
      Button(:numStr="key")
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import Button from '~/components/Button.vue';
// import Logo from '~/components/Logo.vue'

@Component({
  components: {
    Button
    // Logo
  }
})
export default class Index extends Vue {
  keys = [
    'C', '÷', '×', 'del',
    '7', '8', '9', '-',
    '4', '5', '6', '+',
    '1', '2', '3', '=',
    '%', '0', '.',
  ];
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  background: #55b9f3;
  display: grid;
  grid-template-rows: 1fr 15% 15% 15% 15% 15%;
  grid-template-columns: 25% 25% 25% 25%;
}

.gridhead {
  grid-column: span 4;
}
</style>
