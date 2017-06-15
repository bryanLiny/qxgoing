<template>
  <div class="index">
  	<div class="container-fluid">
  		<div class="tab-group row">
  			<div class="col-xs-6 text-center">
  				<a @click="activeTab()" v-bind:class="{active:activeForTab}" href="javascript:;">接机</a>
  			</div>
  			<div class="col-xs-6 text-center">
  				<a @click="activeTab()" v-bind:class="{active:!activeForTab}" href="javascript:;">送机</a>
  			</div>
	  	</div>
	  	<div class="time-select row text-center">
        <a href="javascript:;">
          <img src="../assets/time.png">
          <span>现在</span>
        </a>
	  	</div>
	  	<div class="address-group row">
        <p class="line-addr">
          <img src="../assets/qidian.png">
          <a class="addr-input" href="javascript:;">你从哪儿上车</a>
        </p>
        <p class="line-addr">
          <img src="../assets/zhongdian.png">
          <a class="addr-input last-input" v-bind:class="{active:activeForAddr}" href="javascript:;">厦门高崎T4机场</a>
        </p>
	  	</div>
  	</div>

  </div>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      msg: 'Index',
      activeForTab: true,
      activeForAddr: true
    }
  },
  methods: {
    activeTab: function (type) {
      this.activeForTab = !this.activeForTab
    }
  }
}
</script>

<style scoped>
.tab-group{
	height: 50px;
	line-height: 50px;
	background-color: #fff;
	font-size: 16px;
}
.tab-group a{
	color: #a8abaf;
	text-decoration: none;
	line-height: 50px;
	height: 50px;
	display: inline-block;
	width: 100px;
}
.tab-group .active{
	color: #00b5e6;
	text-decoration: none;
	border-bottom: 1px solid #00b5e6;
}
.time-select{
  background-color: #fff;
  margin-top: 15px;
  height: 50px;
  line-height: 50px;
}
.time-select img{
  width: 16px;
  margin-bottom: 5px;
  margin-right: 5px;
}
.time-select a{
  color: #4b4e51;
  font-size: 16px;
}
.address-group{
  margin-top: 15px;
}
.address-group img{
  width: 10px;
}
.address-group .line-addr{
  line-height: 50px;
  background-color: #fff;
  margin: 0;
  padding-left: 10px;
}
.address-group .addr-input{
  font-size: 16px;
  color: #c5c7ca;
  text-decoration: none;
  margin-left: 15px;
  line-height: 50px;
  width: 80%;
  display: inline-block;
  border-bottom: 1px solid #e5e5e5;
}
.address-group .active{
  color: #4b4e51;
}
.address-group .last-input{
  border-bottom: none;
}
</style>
