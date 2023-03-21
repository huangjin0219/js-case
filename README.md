# js-case：js 小案例

本项目主要记录了一些js的一些小练习和小案例

### [轮播图-简易版](https://huangjin0219.github.io/js-case/轮播图-简易版/demo.html)

思路：n 张图片放在各自的 li 里面，并且定位在 ul 的上层。通过开关控制和加类名的方式实现正常模式和循环模式的切换，通过 display="none"或"block"来控制 li 的显示与隐藏，上一页和下一页的按钮用来控制 li 数组的 index 变化。

主要利用了：

- 设置元素属性：setAttribute
- 移除元素属性：removeAttribute

### [小球的圆周运动-日期格式详解作业](https://huangjin0219.github.io/js-case/小球的圆周运动-日期格式详解作业/demo.html)

思路：计算一下圆点运动时的角度变化即可

主要利用了：transform 和延时器 setInterval

时钟的原理也是类似的。

### DOM 小练习

#### [查找和替换](https://huangjin0219.github.io/js-case/DOM小练习/查找和替换.html)

思路：利用元素的 innerHTML 属性把找到的词用带有特殊样式的 span 标签进行包裹

主要利用了：字符串的 split 和 join 方法

#### [一键导航](https://huangjin0219.github.io/js-case/DOM小练习/一键导航.html)

思路：利用自定义属性按下的每个字符都绑定一个事件

主要利用了：

- 事件监听 addEventListener
- 默认事件的 target 属性：代表目标元素
- 自定义属性设置：dataset

### [360 导航拖拽-鼠标事件](https://huangjin0219.github.io/js-case/360导航拖拽-鼠标事件/demo.html)

思路：使用浮动布局，先把九宫格的布局写好，再根据每个 li 现在所在的位置设置其相应的定位属性，使得布局改为定位布局，然后实现鼠标的拖拽，要有碰撞算法实现拖拽的那个 li 最终应该在哪个位置。

主要利用了：

- 从浮动改为定位布局时，用定时器解决定位元素的覆盖问题。
- 给九宫格添加`mousedown`事件，给整个 document 添加`mousemove`和`mouseup`事件，三个事件**使用同一个函数**。
- 事件的节流与分流

### [网易云音乐 3D 轮播图-自动轮播](https://huangjin0219.github.io/js-case/网易云音乐轮播图/demo.html)

思路：六张图分别在六个 li 里面，给每个 li 添加一个类名，利用 css 把一开始六张图片的位置放好。然后把六个 li 的**类名组成一个数组**，向下翻页就是把数组的最后一位移到第一位，向上翻页就是把数组的第一位移到最后一位。实现自动翻页功能，把向下翻页放在一个定时器里面即可，鼠标移入的时候清除定时器。

主要利用了：

- transform 的 translateX 和 scale
- 数组方法 push pop unshift shift

### [canvas 漂浮动画](https://huangjin0219.github.io/js-case/canvas漂浮动画/demo.html)

思路：

1. 让 canvas 的可绘制区域与浏览器窗口一样大
    1. 获取 canvas 元素
    2. 获取窗口大小
    3. 设置 canvas 宽高属性
    4. 当浏览器窗口大小发生变化时，重新设置canvas 的元素宽高属性 
2. 如何利用 canvas 绘制动态图形
    1. 短时间内连续播放多张图形
      1/60
      `setInterval(function(){},1000/60)`
    2. 每一张图形内部物体的形态必须要发生变化 
3. 绘制 1314 个会动的圆
    1. 大小 颜色 位置 速度 运动方向 都不一样

主要利用了：

- canvas
- es5的构造函数以及原型链
- 生成任意两个数之间的随机数：Math.random() * (max - min) + min

### [改变盒子大小-任意拖拽大小](https://huangjin0219.github.io/js-case/改变盒子大小-任意拖拽大小/demo.html)

思路：跟360导航拖拽类似

css的变量定义


### [移动端图片滑动效果](https://huangjin0219.github.io/js-case/移动端图片滑动效果/demo.html)

基本思路：

1:设置swiper元素里面的ul元素的宽度,使得ul元素的宽度与li的个数进行关联
    1.1:获取swiper下的ul元素
    1.2:获取li元素的个数
    1.3:设置ul元素的宽度

2:设置元素的滑动事件
    2.1:获取触摸ul元素时,手指触摸的位置 x1
    2.2:获取触摸ul元素时,ul元素的位置
    2.3:获取手指滑动时,手指的位置 x2
    2.4:计算ul元素的新位置
    2.5:设置ul元素的新位置

利用了：

- 移动端手指触摸事件：touchstart、touchmove、touchend
- 给元素设置自定义属性：`oUl.transf = {};`
- 关于transform的获取和设置,使用自定义属性，封装一个函数。

### [无缝轮播图](无缝轮播图/demo.html)

前提:有动画效果

逻辑:（这种常规方法，也可以使用更改类名的方式）

- 所有的li横向排列
- 最后一张复制一份到第一张前面
- 第一张复制一份到最后一张的后面
- 当移动到最后一张的后面一张的时候，等动画效果结束后再消除动画并将ul移动到第一张图片的位置，并加上动画，此时的效果就是从最后一张到第一张的切换是平滑的。

利用了：

- 主要就是索引值的辨析
- 动画结束之后执行代码使用的是setTimeout，也可以使用transitionEnd的事件监听，只不过这个事件的兼容性不太好，每个浏览器的对这个事件的名字不同。

### 节点操作

效果：点击热门目的地左右两边同时生成标签，左边有删除，点击删除右边也会同时删除。

主要利用了：
- 自定义属性dataset：用来控制点击热门目的地的开关，第二次点击不能生成一样的标签
- 增加子节点append和appendChild：append可以直接加入文本节点，而appendChild不可以
- 删除自身节点：ele.remove()
- 节点被删除时触发的事件：DOMNodeRemoved

### 淘宝商品信息排序

思路：点击调用排序算法

主要利用了：
- css的伪元素：很多重复的信息可以直接卸载伪元素里面
- 冒泡排序算法
- 快速排序算法