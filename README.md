# canvas 模拟云动画

## 原理分析

## 执行效果
![effect](./effect.png)

## 额外补充
```javascript
window.requestAnimationFrame = (function(){
　　return window.requestAnimationFrame ||    //IE10以及以上版本，以及最新谷歌，火狐版本
　　　　　  window.webkitRequestAnimationFrame ||   //谷歌老版本
　　　　　　window.mozRequestAnimationFrame ||   //火狐老版本
　　　　　　function(callback){    //IE9以及以下版本
　　　　　　　　　　window.setTimeout(callback , 1000/60);  //这里强制让动画一秒刷新60次，这里之所以设置为16.7毫秒刷新一次，是因为requestAnimationFrame默认也是16.7毫秒刷新一次。
　　　　　　}
})();
```
