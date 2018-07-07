<template>
<div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id"><img class="swiper-img" :src="item.imgUrl"></swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
 </div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data () {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true,
					autoplay: 3000
				},
				swiperList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/3b/ef86879aa50e3002.jpg_750x200_2a108508.jpg'
				},{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1706/b8/a8e8ff02b094c802.jpg_750x200_ddaec8e5.jpg'
				},{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/3c/c72a1ccd4d7b2202.jpg_750x200_b88bbab4.jpg'
				}]
			}
		}
	}

</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff !important
	.wrapper
		overflow: hidden
		width:100%
		height:0
		padding-bottom: 27.25%
		background: #eee
		.swiper-img
			width: 100%

</style>