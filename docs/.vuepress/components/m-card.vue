<template>
  <div class="m-card" :style="width ? { width: width + 'px' } : {}">
    <div
      class="m-card-img"
      :style="imgHeight ? { height: imgHeight + 'px' } : {}"
    >
      <img :src="imgSrc" alt="img" />
    </div>

    <div v-if="summary" class="m-card-summary">
      {{ summary }}
    </div>
    <div v-else class="m-card-summary">
      <solt></solt>
    </div>

    <slot class="footer"></slot>
  </div>
</template>

<script>
export default {
  name: 'x-card',
  props: {
    width: {
      type: Number,
      default: 0,
    },
    imgSrc: {
      type: String,
      default: '',
    },
    imgHeight: {
      type: Number,
      default: 0,
    },
    summary: {
      type: String,
      default: '',
    }
  }
}
</script>

<style lang="scss">
@import "./card.scss"
</style>