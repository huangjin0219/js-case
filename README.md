# js-case：js小案例

### DOM小练习
#### 查找和替换

思路：利用元素的innerHTML属性把找到的词用带有特殊样式的span标签进行包裹

主要利用了：字符串的split和join方法

#### 一键导航

思路：利用自定义属性按下的每个字符都绑定一个事件

主要利用了：
- 事件监听 addEventListener
- 默认事件的target属性：代表目标元素
- 自定义属性设置：dataset

### 轮播图-简易版

思路：n张图片放在各自的li里面，并且定位在ul的上层。通过开关控制和加类名的方式实现正常模式和循环模式的切换，通过display="none"或"block"来控制li的显示与隐藏，上一页和下一页的按钮用来控制li数组的index变化。

主要利用了：
设置元素属性：setAttribute
移除元素属性：removeAttribute