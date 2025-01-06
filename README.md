# RippleEffect
基于VUE实现的涟漪特效，类似与ECharts图表里的效果

## How to use
基本使用方法
```vue

<template>
  <div>
    <RippleEffect :symbolSize="ripple.symbolSize.small" :symbolShadow="ripple.symbolShadow" :color="ripple.color" :brushType="ripple.brushType" />
  </div>
</template>

<script>
import RippleEffect from '@/components/RippleEffect'

export default {
  components: {
    ...
    RippleEffect
  },
  data() {
    ...
    ripple: {
        symbolSize: {
          large: 20,
          medium: 15,
          small: 10
        },
        symbolShadow: {
          blur: 0,
          color: '#333'
        },
        color: '#b02a02', // #b02a02 #ddb926 #91cc75
        brushType: 'stroke'
      }
  }
}
</script>

```

### Customize config
配置项说明

* symbolSize
  原点尺寸（直径），单位：px，默认10
* symbolShadow
  原点阴影
  * blur 阴影模糊系数，默认0
  * color 阴影颜色，默认#333
* color
  涟漪颜色，包括原点，默认#b02a02
* number
  波纹数，默认3
* duration
  涟漪持续时长，单位：秒，默认4
* scale
  波纹的最大缩放比例，决定涟漪延伸的距离，默认2.5
* brushType
  波纹的绘制方式，可选值：'fill' - 填充, 'stroke' - 描边，默认fill
