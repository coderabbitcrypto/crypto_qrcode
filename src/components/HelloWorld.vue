<template>
  <div class="container">
    
    <div class="row">
      <div class="col-lg-12">
        <div class="page-header">
          <h3>Crypto - QR Code Generator <small class="text-danger">By Coderabbit</small></h3>
        </div>
      </div>
    </div>
    
    <div class="row">
      <div class="col-lg-4"><img :src="img" :width="size" alt=""></div>
      <div id="frm-data" class="col-lg-8">
        <div class="form-group">
          <input type="text" class="form-control" v-model="coin_addr" id="coin_addr" placeholder="Bitcoin Address">
        </div>
        <div class="form-group">
          <input type="text" class="form-control" v-model="coin_amount" id="coin_amount" placeholder="Amount to be requested (Optional)">
        </div>
        <div class="form-group">
          <fieldset>
            <legend>Data Redundancy</legend>
            <label for="l_opt" class="lbls"><input type="radio" v-model="l_opt" value="L">&nbsp;&nbsp;7%</label>
            <label for="l_opt" class="lbls"><input type="radio" v-model="l_opt" value="M">&nbsp;&nbsp;15%</label>
            <label for="l_opt" class="lbls"><input type="radio" v-model="l_opt" value="Q">&nbsp;&nbsp;25%</label>
            <label for="l_opt" class="lbls"><input type="radio" v-model="l_opt" value="H">&nbsp;&nbsp;30%</label><br />
            <small class="text-primary">Proportion of the image which can be hidden/modified without altered the code.</small>
          </fieldset>
        </div>
        <div class="form-group">
          <button class="btn btn-success" v-on:click="makeQrCode"><i class="fa fa-search"></i>&nbsp;&nbsp;&nbsp;Check Balances</button>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      img: null,
      coin_addr: "",
      coin_amount: "",
      l_opt: 'H',
      size: 300
    }
  },
  methods: {
    makeQrCode(){
      var _addr = "bitcoin:"+this.coin_addr;
      if(this.coin_amount>0){
        _addr +="?amount="+this.coin_amount;
      }
      this.img = "https://chart.googleapis.com/chart?cht=qr&chs="+this.size+"x"+this.size+"&chl="+_addr+"chld="+this.l_opt;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.lbls{
  margin-right: 1.8rem;
}
</style>
