###js入门
---
###1.1 调试
* alert（value）；    
alert（value）可以弹出一个提示框，弹出的内容就是写在括号里value的内容   
alert 是用来调试代码的

注意：一般不建议使用行间样式写js

###1.2 注释
* /* 多行注释 */
* // 单行注释

###1.3 事件绑定
* document （文档）
* '.' （的）
* get  (获取)
* element （元素）
* by（通过）
* id（id名称）
* function  （函数）    
函数可以理解为一个盒子，盒子里装有很多需要做的事情，这些事情默认不会执行，当把函数绑定给事件，事件进行调用函数的时候，函数才会执行


###1.3.1 简单事件
* onclick 鼠标点击事件
* onmouseover 鼠标移入事件
* onmouseout  鼠标移出事件
###1.4 属性操作
<pre>
var box1 = document.getElementById（'box1'）; //获取id名称
box1.onclick = function（）{
	box1.style.background = 'red';  //给点击box1添加样式
};
</pre>
<pre>
var box1 = document.getElementById（'box1'）; //获取id名称
box1.onmouseover = function（）{
	box1.style.background = 'yellow;  //鼠标移入box1 改变颜色
};
</pre>
<pre>
var box1 = document.getElementById（'box1'）; //获取id名称
box1.onmouseout = function（）{
	box1.style.background = 'yellow;  //鼠标移出box1 改变颜色
};
</pre>
###1.5 变量
* var （用来声明变量的）      
变量是用来保存内容的
* 变量命名规范   
1、首位不能说数字   
2、一些特殊符号不能用   
3、关键字、保留字不能用     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;关键字是系统中有特殊含义的字符  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;保留字，目前还不是关键字，以后可能成为关键字。
<pre>
var a1 = 11111111111;
alert(a1);  //弹出的结果就是11111111111
</pre>
###1.6 属性操作
<pre>
var box = document.getElementById（'box'）;
box.style.background-color = 'red';   //这样的属性写法是错误的
正确写法
box.style.backgroundColor = 'red';  //需要把属性中间的'-'去掉，并第二个单词首字母大写
box.style['background-color'] = 'red';  //如果不去掉'-',需要在属性外加[]

var W = width;   //声明变量保存属性
box.style[W] = '100px';  //变量名外要加[]，其中切不要加引号
</pre>
###1.7 例子
* [ ]可以代替'.'，但是'.'不能代替[]
* 属性操作：   
读操作：直接访问属性，获取属性的值   
写操作：修改属性的值，属性=属性值
<pre>
一个input的value与另一个input的value相加得出的结果

var text1 = document.getElementById（'text1'）;
var text2 = document.getElementById（'text2'）;
var btn = document.getElementById（'btn'）;
var text3 = document.getElementById（'text3'）; 
btn.onclick = function（）{
	text3.innerHTML = text1.value+text2.value;
};

</pre>
###1.8 字符串
* 字符串：一对双引号" "或者一对单引号' '所包含的零个或者多个字符
* 引号中没有任何字符叫做空字符串
* 赋值操作会覆盖已有的值，innerHTML的赋值操作会把以前的元素替换掉，即使表面看起来一样，但实际已经不是以前的那个元素了
<pre>
document.body.innerHTML = 1;  // 如果document.body.innerHTML 之前是有元素的，那么现在已经替换成1了
document.body.innerHTML = 1 + document.body.innerHTML;//如果想要之前元素还存在，那么就必须加上之前的innerHTML
document.body.innerHTML+= 1 ; //这样写也可以
</pre>
* class 是关键字   
所以操作一个元素的class我们使用className来代替
<pre>
例如：样式里写个class名字为.color，其中写上需要添加的样式属性
JS中进行调用： box.className = '.color';
</pre>
* Float （浮动）  
标准浏览器：cssFloat  
IE浏览器：styleFloat
###1.8 字符串拼接
 
 * num++; 自增运算符，每次num+1;
 * num--;自减运算符，每次num-1;

<pre>
var num = 0;
document.onclick = function(){
num++;
document.body.innerHTML += 'div前标签'+num+'div后标签';
};
</pre>
### if 语句
* true （代表真）
* false （代表假）
* if 语法
<pre>
if（判断条件）{
	条件成立的时候执行的代码
}else{
	否则走这里的代码
}
</pre>
* > 大于
* < 小于
* >= 大于等于
* <= 小于等于
* == 等于

<pre>
if(box.style.display == 'none'){  //条件判断
	box.style.display = 'block';  // 如果成立就执行这个
}else{							// 否则 就走下一行
	box.style.display = 'none';
}
</pre>
<pre>
var box = document.getElementById（'box'）;
数字0代表none；
数字1代表block；
var num = 0 ；如果没有条件就自己创建条件
if（ num == 0）{
	box.style.display = "block";
	num = 1；
}else{
	box.style.display = "none";
	num = 0；
}
</pre>
<pre>
var box = document.getElementById（'box'）;
var onOff = flase；  //设置开关
document.onclick = function（）{
	if（onOff == flase ）{
		box.style.display = 'block'；
		onOff = true;
	}else{
		box.style.display = 'none';
		onOff = false;
	}
}
</pre>