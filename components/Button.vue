<template lang="pug">
  button.button(@click="handleClick") {{ numStr }}
</template>

<script lang="ts">
import { Component, Prop, Vue } from "nuxt-property-decorator";

@Component
export default class Button extends Vue {
  @Prop({ type: String, required: true})
  public numStr!: String;

  public handleClick() {
    console.log(this.$props.numStr)
  }
}
</script>

<style lang="scss" scoped>
.button {
  width: 80px;
  height: 80px;
  border-radius: 50px;
  font-size: 2.2rem;
  color: #f3f3f3;
  background: linear-gradient(145deg, #4da7db, #5bc6ff);
  box-shadow:  20px 20px 60px #479bcc, 
               -20px -20px 60px #63d7ff;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  outline: none;
  appearance: none;
  border: none;
}
</style>
