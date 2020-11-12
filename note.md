项目准备
1.样式重置与模块化
2.line-height不同值的区别
3.css @规则
4.favicon
5.base标签
6.自定义图标
7.H标签的应用场景
8.以图换字
9.怪异盒模型（IE盒模型）
10.css3 （圆角、渐变、过渡）
11.IE滤镜
12.CSS Sprites
15.表格
16.图片格式 webp
17.词换行

```css
body{
	font: 12px/1.5 tahoma,arial,'Hiragino Sans GB','\5b8b\4f53',sans-serif;
}

font-family:'\5b8b\4f53' 代表 宋体 


清除浮动

.clearfix : after{
	content : ' ' ;
	display：block；
	clear：both；
}
```

@规则
@charset     设置样式表的编码
@import      导入其他样式文件
@meida       媒体查询
@font-face  自定义字体

<link rel="icon" href="图标地址">

<base href=" " target="_black">

属性 target="_blank" 在新页面中打开网页

iconfont 阿里巴巴矢量图标库
代码应用https://www.iconfont.cn/help/detail?spm=a313x.7781069.1998910419.16&helptype=code


盒模型
1.标准盒模型
总宽度=border（左右）+width+padding（左右）
总高度=border（上下）+height+padding（上下）
2.IE盒模型（怪异盒模型）
总宽度=width；
总高度=height；
box-sizing：border-box；

按钮
<button type="submit">搜索</button>

输入框
<input type="text">
outline：none；轮廓

<form action="#">
	...
</form>


```css

text-indent: -9999px;
/* 首行缩进 */

cursor：pointer；

border-radius：x y z w；


背景颜色渐变

background-image：linear-gradient(to right，#f9000，#ff5000);

linear-gradient （...）表线性渐变
to right 表示从左往右渐变


IE滤镜
filter：；

filter: progid:DXImageTransform.Microsoft.gradient
(startColorstr='#ffff9000', endColorstr='#ffff5000', GradientType=1);


width：calc（100% - n px）；n表示任意数  ！运算符号前后必须有一个空格！！！
兼容性 IE9+

border-sizing：border-box； ！！！

transition：background-color 0.3s；
【CSS3 transition 属性】https://www.w3school.com.cn/cssref/pr_transition.asp


background-color：rgba（0,0,0,0.3） 兼容性 IE9+
		<--->
background-color：#000\9;    IE9以下的浏览器认识
filter：alpha（opacity=30）; 透明度

图片垂直居中
 . img{
	display：table-cell；
	vertical-align：middle；
}

弹性布局（弹性盒模型）  兼容性 IE10+
 . img{
	display：flex；
	justify-content：space-around；   水平居中
	align-items：center；                    垂直居中
}

 
background position！
background：#ffe4dc url（../images/ico.png）0 -572px no-repeat；


表格
<table class="#">
	<tr>
		<td class="#">
			...
		</td>
	</tr>
</table>

表格重置
table{
	border-collapse：collapse；  /*边框模式，合并模式*/
}

th，td{
	...
}

table-layout：fixed；    /*定义列宽的算法，
                                      fixed的计算方式为个根据表格宽度自动计算列宽,
                                      每列的宽度均分整个表格的宽度*/

word-break：keep-all；   空格强制换行

```