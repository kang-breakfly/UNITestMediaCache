## UNITestMediaCache
###  1、引用
var cacheModel = uni.requireNativePlugin("XD-HttpProxCache")

###  2、使用说明
 该缓存、预加载、边播边存的插件对播放器没有限制，只需要把链接地址传进来，插件把处理后的地址返回去，直接使用插件处理后的地址就可以播放，对原有的界面播放器不用做调整。

###  3、方法介绍

方法1、默认预缓存进度是30% 缓存方法 ， 传入音视频数组，类型可以是 字符串数组或者字典数组（如果是字典数组，需要缓存的key值位 url）

defaultPreloadWithUrls

调用方式
 cacheModel.defaultPreloadWithUrls(list,(res)=>{
	console.log('*****'+res)
 })


方法2、 缓存方法 传入音视频数组，类型可以是 字符串数组或者字典数组（如果是字典数组，需要缓存的key值位 url）,在传入预缓存百分比（最大是1），返回值是 替换后url的原数据数组
preloadVideoWithUrls:(list)

调用方式
cacheModel. preloadVideoWithUrls(list,0.2,(ret)=>{

})

方法3、传入一个 音视频url地址 返回缓存的url地址
assetURLWithURL

调用方式
cacheModel. assetURLWithURL(url,(ret)=>{

})
