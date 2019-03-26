# canvas-merge-video-in-vue

## [demo](https://spademan.github.io/seamlessCanvasPlayer/#/)

## 一.组件形式使用

### 组件引入方式

```
1.npm install seamlessCanvasPlayer --save

```
### html文件中
```
import seamlessPlayer from 'seamlessCanvasPlayer'
Vue.use(seamlessPlayer)

```

```
<template>
  <div id="app">
    <merge-video :playList='playList' :autoPlay='autoPlay' :audioSrc='audioSrc'></merge-video>
  </div>
</template>

```

```
autoPlay: false, // 是否自动播放 Boolean(required)
playList: [] // 碎片列表 Array（）
sounds: Number// 声音 Number（非必填）
audioSrc: String// 第三方声音（必填）
poster: '' // 海报图
height: '' // 播放器高
width: '' // 播放器宽
picOption: { // 水印配置
  editLogo: false, // // 是否需要调整水印
  logoSrc: require('./assets/logo.png'), //水印地址
  info: {
    w: 60, // 宽
    h: 60, // 高
    x: 0 // logo相对画布x轴起点
    y: 0 // logo相对画布y轴起点
  }
},
```
##二. fork项目跑起来 (想自己改造源码的同学可以看这个步骤)
``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```
### 此pro注意点：
```
1.并没有考虑性能
```
### Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

```

### 存在问题

2.播放过程拖拽会出现跳帧去情况，导致播放条秒数不太准确

2.不兼容移动端

3.后续canvas转场效果会补上

4.全屏功能

### 参考
https://www.w3.org/2010/05/video/mediaevents.html

https://github.com/spademan/canvas-merge-video-in-vue
