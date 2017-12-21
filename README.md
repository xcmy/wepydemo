## WePY项目


[官方文档](https://tencent.github.io/wepy/)
[github地址](https://github.com/Tencent/wepy)



## 按照👆指导步骤初始化项目

## 在pages创建自己的主页home.wpy


```vue
<style lang="less">

</style>
<template>
  <view class="container" >

    <text class="info">{{step.count}}</text>
    <text class="info">今天为本群点击的次数</text>
    <!--<image style="width: 200px; height: 200px; background-color: #eeeeee;" mode="{{item.mode}}" src="{{step.img}}"></image>-->

    <button @tap="tap" size="default" type="primary">点击木鱼</button>

  </view>

</template>

<script>
  import wepy from 'wepy'
  import howler from 'howler'
  export default class Home extends wepy.page {

    data = {
        step:{
          count:0,
          img:"../image/1.jpg"

  }
    }
    methods = {
      tap(){
        this.step.count++
        this.play()
      },
      play(){
        console.log("播放")
        // var sound = new Howl({
        //   src: ['sound.webm', '../audio/chengdou.mp3']
        // });
        // sound.play()
      }
    }

  }
</script>

```

## 修改app.wpy中入口文件为home.wpy

## 打开小程序可以看到变化
