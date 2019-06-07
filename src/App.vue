<template>
  <div id="app" @touchmove.prevent>
    <v-header :seller="seller"></v-header>
    <div class="tab-wrapper">
      <tab :tabs="tabs"></tab>
    </div>
  </div>
</template>

<script>
  import VHeader from 'components/v-header/v-header'

  export default {
    components: {
      VHeader
    }
  }
</script>

<style lang="stylus" scoped>
</style>
