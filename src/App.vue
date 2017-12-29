<template>
  <div id="app">
    <CryptoQRCode/>
  </div>
</template>

<script>
import CryptoQRCode from './components/CryptoQRCode'

export default {
  name: 'app',
  components: {
    CryptoQRCode
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#frm-data{
    line-height: 4.4rem;
}
</style>
