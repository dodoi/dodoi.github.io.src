---
title: 微信小程序-尺寸单位rpx
date: 2017-01-19 16:43:38
tags: [前端,小程序]
---


rpx单位是微信小程序中css的尺寸单位，rpx可以根据屏幕宽度进行自适应。

#### Iphone设备相关参数

设备          | 屏幕尺寸 |分辨率(PT) |Reader  |分辨率(px) |渲染后    |PPI(DPI)
---           |---       |---        |---     |---        |---       |---
iPhone 3GS    | 3.5寸    | 320*480   |@1x     |320*480    |空        |163
iPhone 4/4S   | 3.5寸    | 320*480   |@2x     |640*960    |空        |326
iPhone 5/5S/5C| 4.0寸    | 320*568   |@2x     |640*1136   |空        |326
iPhone 6/6S   | 4.7寸    | 375*667   |@2x     |750*1334   |空        |326
iPhone 6P     | 5.5寸    | 414*736   |@3x     |1242*2208  |1080*1920 |401


- pt:逻辑分辨率； pt的大小与屏幕的尺寸有关系，简单可以理解为长度和视觉单位
- px指物理分辨率,和屏幕尺寸没关系
####  pt和px关系
- 1个pt可以有1个px构成，也可以有2个px,还可以有3个甚至更多
- Iphone6是由2个px构成的。
-

#### 如何做不同分辨率设备的自适应
- 以iphone6的物理像素750*1334为视觉稿进行设计，而在小程序中使用rpx为单位
- iphone6下  1px = 1rpx = 0.5pt
- 使用rpx小程序会在不同分辨率的设备下自动进行转换，而px不会

建议设计团队按iphone6来做设计图,因为
Iphone6 1px=1rpx
Iphone6 plus 1px=0.6rpx
Iphone6换算比较方便。

不是所有的单位都适合rpx，字体不适合rpx,会导致不同设备看不清
