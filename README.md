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