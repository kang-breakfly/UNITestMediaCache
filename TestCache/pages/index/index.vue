<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
			
		</view>
		<view>
			<button type="primary" @click="testModel">testModel</button>
			</view>
	</view>
</template>

<script>
	var cacheModel = uni.requireNativePlugin("XD-HttpProxCache")
	
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
testModel(){
	
		
	if(cacheModel == null){
		//var word = model.testUniModelWith("张三")
		 
		 
		
			this.title = "null "
	}else{
			
	// var result =	cacheModel.testUniModelWith({"name":"张三"})
		
		
		// cacheModel.defaultPreloadWithUrls(["https://videos-1300576043.file.myqcloud.com/eb54bb45bbc1ff29c8484addb017f175.mp4"],(res)=>{
		// 	console.log('*****'+res)
		// })
		
	 cacheModel.preloadVideoWithUrls(["https://videos-1300576043.file.myqcloud.com/eb54bb45bbc1ff29c8484addb017f175.mp4"],0.2,(res)=>{
	 	console.log('------'+res)
	})
		
		//var word = cacheModel.testUniModelWith("张三")
		
		//print('---')
		//print(model)
			// this.title = result
			
			
			//
			
			
			//var cache =  VIMediaCache()
			//console.log(cache+"")
	}
	
	
	// this.setData({
	// 	title : "张三"
		
	// })
	console.log('------')
	console.log(cacheModel+"")
}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
