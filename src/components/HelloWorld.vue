<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-12">
        <div class="page-header">
          <h3>Balance Checker <small class="text-danger">Only for Bitcoin Addresses</small></h3>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="form-group">
        <div class="col-lg-12">
          <label class="control-label" for="wallet_addrs">Wallets Addresses</label>&nbsp;&nbsp;&nbsp;<em class="text-success">separated by comma</em>
        </div>
        <div class="col-lg-10">
          <input type="text" class="form-control" name="wallet_addrs" id="wallet_addrs">
        </div>
        <div class="col-lg-2">
          <button class="btn btn-success"><i class="fa fa-search"></i>&nbsp;&nbsp;&nbsp;Check Balances</button>
        </div>
      
      </div>
    </div>
    <hr>
    <div class="row">
      <div class="col-lg-12">
        <h3>XXXXXXX</h3>
      </div>
      <div class="col-lg-10">
        Current Balance: <strong>XXXXXXX</strong><br />
        Total Received: <strong>XXXXXXX</strong><br />
        Total Sent: <strong>XXXXXXX</strong><br />
        Total Tx.: <strong>XXXXXXX</strong>
      </div>
      <div class="col-lg-2">
        <button class="btn btn-primary" data-url=""><i class="fa fa-external-link"></i>&nbsp;&nbsp;&nbsp;Details</button>
      </div>
    </div>

    <div class="row"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
