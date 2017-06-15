<template>
  <div class="index">
  	<div class="container-fluid">
  		<div class="tab-group row">
  			<div class="col-xs-6 text-center">
  				<a class="active" href="javascript:;">接机</a>
  			</div>
  			<div class="col-xs-6 text-center">
  				<a href="javascript:;">送机</a>
  			</div>
	  	</div>
	  	<div class="time-select">
	  	</div>
	  	<div class="address-group">
	  	</div>
  	</div>

  </div>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      msg: 'Index'
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
</style>
