<template>
	<view class="content">
		<!-- <image class="main-img" src="../../static/imgs/main-img.jpg" mode=""></image> -->
		
		<div class="propagate-text">
			<div>一起来打全场</div>
			<div>This is for You</div>
		</div>
		
		<div class="into-button" @click="toHome">开始组队</div>
	</view>
</template>
<script>
	export default{
		methods:{
			toHome() {
				uni.redirectTo({url: '/pages/home/index'})
			}
		}
	}
</script>
<style lang="scss" scoped>
	.content{
		// background-color: black;
		background: url('../../static/imgs/main-img.jpeg') no-repeat center;
		background-size: cover;
		height: 100vh;
		width: 100vw;
		position: absolute;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		.main-img{
			width: 100%;
		}
		.propagate-text{
			margin-top: 50rpx;
			margin-bottom: 127rpx;
			font-family: cursive;
			color: #1d1810;
			text-align: center;
			font-size: 60rpx;
			animation:textScale 2s ease-in
		}
		.into-button{
			margin-top: 80rpx;
			background-color: #de8d05;
			height: 120rpx;
			line-height: 100rpx;
			width: 300rpx;
			border: 7rpx solid #6b2807;
			border-radius: 6rpx;
			margin: 0 auto;
			// color: #6b2807;
			font-size: 60rpx;
			text-align: center;
		}
	}
	@keyframes textScale
		{
			0% {
				transform:scale(0.2, 0.2);
				opacity: 0.2;
			}
			// 50% {
			// 	transform:scale(1.5, 1.5);
			// 	opacity: 1;
			// }
			100% {
				transform:scale(1, 1);
				opacity: 1;
			}
		}
</style>