<template>
  <div class="container">
    <div class="col">
      <slot></slot>
    </div>
  </div>
</template>
<script>
export default {
  name: 'card-text',
  data () {
    return {
      keepAlive: true
    }
  },
  beforeMount () {
    if (this.$parent.$options._componentTag !== 'm-card') {
      console.error('Cannot use card-title outside of m-card. \nSee https://www.npmjs.com/package/vue-mstyle for more details.')
      this.keepAlive = false
    }
  }
}
</script>
