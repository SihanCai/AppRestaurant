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
  import {getSeller} from 'api'

  export default {
    name: 'app',
    data() {
      return {
        seller: {

        }
      }
    },
    created() {
       getSeller().then((seller) => {
         this.seller = seller
       })
    },
    components: {
      VHeader
    }
  }
</script>

<style lang="stylus" scoped>
</style>
