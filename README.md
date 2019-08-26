## VueDemo

## Vue的使用场景：单页应用程序

前提：导入Vue的js文件

当我们导入包之后，在浏览器的内存中就多了一个Vue构造函数

创建一个Vue的实例

```javascript
var vm = new Vue({
    el:,//表示当前的实例对象，要控制页面中的哪个区域
  	data:{//存放el中要用到的数据
    	msg:'aaa',
	},
    method:{
       changeNum(){}         
  	}//
})
```

### 插值

#### 插值表达式：{{}};

注意：在Nextwork中为slow 3G时，页面会出现闪烁问题；`{{msg}}`
解决办法：元素属性中使用v-cloak,然后在CSS样式中加入[v-cloak]{display:none};

- `v-` 前缀作为一种视觉提示，用来识别模板中 Vue 特定的特性。

##### v-once

执行一次性地插值，当数据改变时，插值处的内容不会更新

##### v-cloak指令

解决插值表达式的闪烁问题；

##### v-text指令

在元素中插入对应的内容；`v-text='msg'`

##### v-html指令

在元素中插入对应的内容；`v-html='msg'`

##### v-bind指令

用于绑定属性的指令；`v-bind:value='msg'`可以简写为`:value='msg'`
可以写合法的js方法

> 三种用法
>
> 1. 直接使用指令`v-bind`
> 2. 使用简化指令`:`
> 3. 在绑定的时候，拼接绑定内容：`:title="btnTitle + ', 这是追加的内容'"`