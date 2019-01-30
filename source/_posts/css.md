---
title: CSS
date: 2018-11-30
tags: [css, fontend]
cover: /img/post-cover/3.jpg
---

# CSS

```html
<linkrel="stylesheet" type="text/css" href="">
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

rel  要参照外部文档

type 文档类型



离文本越近的的样式，优先级越高。

<link >如果放在<style>下面，则会优先显示<link>中的内容。如果此时<pstytle="">，则显示<p>中的style样式。



CSS语法：

1. 单一元素的多个属性之间用分号分开，多个元素之间用逗号分开
2. 若值为若干元素，则要给值加引号；除这种情况以外其他时候不加引号
3. 样式的优先顺序：

设计者设计的样式>浏览器用户自定义的样式>浏览器自设的样式

强制优先级：！important

1. 行内(内联)样式
2. 内部样式：style中的样式
3. 外部样式

1. 层叠、继承、冲突

外观样式--比如字体、颜色可以继承；而布局有关的样式不可以继承，比如边框等

```html

```

<div>div中的html5

<p>p中的html5</p>

</div>

//<p>继承了<div>的样式

​    \5. 可以在同一个HTML文档内部引用多个外部样式表



**6-4 常用选择器：**

通用选择器：*

元素选择器：p{}

id选择器：#id{}

类选择器：

```html
<h3 class="class1">h里的内容</h3>
<p  class="class1">p里的内容</p>
<div  class="class1 class2" id="div1">div里的内容</div>
.class1{}
.class2{}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



**6-5 属性选择器**



```html
input[value]{background:green}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

E[att] :

E[att="val"]：选择具有att属性且属性值等于val的E元素。进一步缩小选择范围，（只选择有特定属性值的元素。）

E[att~="val"]:选择具有att属性且属性值有多个，其中一个的值等于val的E元素。

E[att|="val"]:选择具有att属性且属性值为以val开头并用连接符"-"分隔的字符串的E元素。

E[att^="val"]:选择具有att属性且属性值为以val开头的字符串的E元素。

E[att$="val"]:选择具有att属性且属性值为以val结尾的字符串的E元素。

E[att*="val"]:选择具有att属性且属性值为包含val的字符串的E元素。

```html
input[value][style]{background: green}
input[value='vip1']{background: red}
input[style~='15px']{background: red}
p[lang|="en"]{color: red}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







**6-7 关系选择器**

后代选择器(包含选择器)：ul li{}

```html
ul li{color: red;border: 1px solid}
div p{color: green}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

子元素选择器:

```html
ul>li{border:2px pink solid}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

相邻选择器：

E+F:选择紧贴在E元素之后F元素。

h2+p{color:green}

兄弟选择器

E~F:选择E元素所有兄弟元素F。(只可以选择到之后的元素)

h2~p{color:purple;}



**6-8**

伪元素选择器:

E:first-letter/E::first-letter设置元素内的第一个字符的样式。

p::first-letter{font-size:30px}

E:first-line/E::first-line设置元素内的第一行的样式。

p::first-line{color:red}

E:before/E::before在每个E元素的内容之前插入内容。用来和content属性一起使用

E:after/E::after在每个E元素的内容之后插入内容。用来和content属性一起使用

a::before{

content: "click"

}

a::after{

content:url(jay50px.jpg);

}

E::selection设置对象被选择时的颜色。

p::selection{color:pink}



**6-9 伪类选择器**

E:first-child父元素的第一个子元素E。



li:first-child{color: green}  //是li元素，也是第一个子元素

![img](https://img-blog.csdn.net/20180423171116963?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xlYXJuX2luQ1NETg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

```html
ul>li:first-child{color: pink} //也可以配合ul>li使用
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

:root:选择文档的根元素（html就是根元素）

:root{background:green}

E:last-child:最后一个子元素E。

E:only-child:仅有的一个子元素E。

E:only-of-type:只有一种类型的子元素。

E:nth-child(n):匹配父元素的第n个子元素E。

```html
h3:nth-child(2){color: red}
#div1>h3:nth-child(2){color: red}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

E:nth-last-child(n):匹配父元素的倒数第n个子元素E。

E:first-of-type:匹配同类型中的第一个同级元素E。

E:last-of-type:匹配同类型中的最后一个同级元素E。

E:nth-of-type(n):匹配同类型中的第n个同级兄弟元素E。

E:nth-last-of-type(n):匹配同类型中的倒数第n个同级兄弟元素E。

E:empty:匹配没有任何子元素（包括text节点）的元素E。

```html
div:empty{width: 500px; height: 100px;background: pink}
/* 与div的id无关，自动识别的,此时id设置为“111” */
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



**6-11  UI伪类及其他选择器**

E:active向被激活的元素添加样式。

E:hover 当鼠标悬浮在元素上方时，向元素添加样式。

E:link向未被访问的链接添加样式

E:visited向已被访问的链接添加样式。



E:focus向拥有键盘输入焦点的元素添加样式。

E:lang向带有指定 lang 属性的元素添加样式。

input:checked选择每个被选中的input元素。

```html
input:checked{background: red;width: 60px; height: 60px}
/* 当被选中的时候出现样式 */
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

input:disabled选择每个禁用的input元素





html:      

```html
<p>
	<input type="password" name="password" id="password" placeholder="密码" disabled="">
	<label for="password">密码</label>			
</p>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

css:



```html
input:disabled{background: red}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

input:enabled选择每个启用的input元素。

input:disabled选择每个禁用的input元素

\#E:target选择当前活动的锚点元素。

在HTML页面的<style>中添加

:not(E)选择E元素之外的每个元素。

:not(input){color:green}



**6-13 选择器的优先级**

原则上：元素选择器<类选择器<ID选择器<行内样式

谁只想精确谁的优先级高

并列的话谁再后面谁的优先级高



**6-14**

三种颜色表示方式：

```html
#div1{background: red}
#div2{background: #ff8800}
#div3{background: rgb(200,200,255);}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. RGBA方式三原色配色方式



在RGB模式上新增了Alpha透明度。

```html
#div4{background: rgba(150,10,0,0.1);}     //0-1：透明-不透明
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. HSL模式

语法:HSL(H,S,L)，HSL分别表示色调，饱和度，亮度

H:0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值来指定颜色。取值为：0 - 360

S:(饱和度)。取值为：0.0% - 100.0%

L:(亮度)。取值为：0.0% - 100.0%

```html
#div5{background:hsl(125,50%,80%)}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. HSLA模式





> > HSL模式上新增了Alpha透明度。

```html
#div6{background:hsla(125,50%,80%,0.5);}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



**6-16**

1. font-size 规定文本的字体尺寸

通常使用px,百分比，em来设置字体的大小

```html
#div1{font-size: 20px}
#div2{font-size: 100%}
#div3{font-size: 3em}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



(em是css中的相对单位，是相对于当前对象内的字体尺寸，若没有制定文字大小尺寸，则为浏览器默认字体大小)



xx-small、x-small、small、medium、large、x-large、xx-large把字体的尺寸设置为不同的尺寸，默认值：medium。

smaller把 font-size 设置为比父元素更小的尺寸。

arger 把font-size 设置为比父元素更大的尺寸。

```html
#div4{font-size:xx-small;}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. font-variant:规定是否以小型大写字母的字体显示文本。

normal默认值。浏览器会显示一个标准的字体。

small-caps浏览器会显示小型大写字母的字体。



1. font-style:规定文本的字体样式。

normal默认值。浏览器会显示一个标准的字体。

italic 浏览器会显示一个斜体的字体样式。

oblique浏览器会显示一个倾斜的字体样式。暂时不作讲解，了解即可



1. font-weight:规定字体的粗细。

normal默认值。定义标准的字符。

bold 定义粗体字符。

bolder定义更粗的字符。lighter 定义更细的字符。

100-900;定义由粗到细的字符。400 等同于 normal，而 700 等同于 bold。

```html
#div6{font-variant: small-caps;}
#div7{font-style: italic;}
#div8{font-weight: 900;}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. font-family:规定文本的字体系列。

```html
#dic9{font-family: 隶属,楷体,微软雅黑;},微软雅黑;}
```



1. font:在一个声明中设置所有字体属性。

这个简写属性用于一次设置元素字体的两个或更多方面。

至少要指定字体大小和字体系列

可以按顺序设置如下属性：font-style/font-variant/font-weight/font-size/font-family

```html
font-size/font-family  这个必须要写
#div10{font:bold small-caps 50px 微软雅黑}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



@font-face:嵌入字体 

注：字体的设置还有其他几个很少的用到的属性，比如font-size-adjust为元素规定 aspect 值；font-stretch收缩或拉伸当前的字体系列。都很少用到或者多数浏览器不支持，就不作讲解







6-18  有字库(www.youziku.com)



6-19 文本属性--掌握

1. color 设置文本颜色
2. text-align 规定元素中的文本的水平对齐方式。

left 默认值/right/center/justify两端对齐

CSS3中新增了start和end属性值，在通常情况下，start相当于left，end相当于right

1. line-height 设置行高。

normal/数字/百分比/px/em

1. text-indent 设置文本的首行缩进

常用单位像素/百分比/em

1. text-decoration 向文本添加修饰。

none 默认值。显示标准的文本。

underline 定义文本下划线。

overline 定义文本上划线。

line-through 定义穿过文本下的一条线。

blink 定义闪烁的文本。

CSS3中还有一些新增加的属性值但是目前浏览器多不支持，不再介绍

1. letter-spacing 设置字符间距。

定义字符间的固定空间

normal 默认。/像素：（允许使用负值）

1. word-spacing 设置字/单词间距。

增加或减少单词间的空白

normal 就等同于设置为 0。/如果指定为长度值，会调整字之间的通常间隔；（允许使用负值）。

1. text-transform 设置对象中的文本的大小写

none默认。标准的文本。/capitalize每个单词以大写字母开头。/uppercase 转换为大写字母。/lowercase转换为小写字母

1. text-shadow 向文本添加阴影。

```html
text-shadow: 4px 4px 1pxrgba(255,0,0,0.6);   //阴影透明
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



**6-22  文本属性--熟悉**

1. white-space 设置元素中空白的处理方式。

normal 默认。空白会被浏览器忽略

pre 空白会被浏览器保留。其行为方式类似 HTML 中的pre标签。

nowrap 文本不会换行，文本会在在同一行上继续，直到遇到br标签为止。

pre-wrap 保留空白符，但是正常地进行换行。

pre-line 合并空白符，但是正常地进行换行。

1. direction 设置文本方向

ltr默认。文本方向从左到右。/rtl 文本方向从右到左。

1. word-wrap 允许对长的不可分割的单词进行分割并换行到下一行。

normal默认值/break-word:在长单词或 URL 地址进行换行。

1. word-break 规定非中日韩文本的换行规则。

normal默认值/break-all：允许在单词内换行。/keep-all 只能在半角空格或连字符处换行。

1. text-fill-color 文本填充颜色，指定文字填充部分的颜色.目前多数浏览器不支持，暂不讲解。
2. text-stroke 文本边框颜色，指定文字描边部分的颜色。目前多数浏览器不支持，暂不讲解。

text-stroke-width文字的描边宽度

text-stroke-color文字的描边颜色

备注:使用该属性需要使用浏览器私有前缀

1. text-overflow 设置是否使用一个省略标记（...）标示对象内文本的溢出

clip：默认值当对象内文本溢出时不显示省略标记（...），而是将 溢出的部分裁切掉。

ellipsis：当对象内文本溢出时显示省略标记（...）。

温馨提示:该属性需要和over-flow:hidden属性、white-space:nowrap配合使用。



**6-23 文本属性--了解**

1. text-outline 规定文本的轮廓
2. text-justify 规定当 text-align 设置为 "justify" 时所使用的对齐方法。
3. text-align-last 设置如何对齐最后一行或紧挨着强制换行符之前的行。
4. text-emphasis 向元素的文本应用重点标记以及重点标记的前景色。
5. unicode-bidi 用于同一个页面里存在从不同方向读进的文本显示。与direction属性一起使用

normal/embed/bidi-override

不常用，了解即可

1. hanging-punctuation 规定标点字符是否位于线框之外。
2. punctuation-trim 规定是否对标点字符进行修剪。
3. tab-size:设定一个tab在页面中的显示长度
4. text-wrap 规定文本的换行规则。注释：目前主流浏览器都不支持 text-wrap 属性。









**6-24 css3前缀**

W3C标准

```html

```







```html
#p2{
	font-size: 50px;
	text-stroke:2px red;      //这种写法防止有的浏览器识别有的浏览器不识别
	text-fill-color:green;
	-webkit-text-stroke:2px red;       //字体描边红色
	-webkit-text-fill-color:green;       //字体填充绿色
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



**6-25  css盒模型**



盒模型的概念：

CSS 盒模型规定了处理元素内容、内边距、边框 和 外边距 的方式。

最内部分是元素内容，直接包围内容的是内边距。内边距呈现了元素的背景。内边距的边缘是边框。边框以外是外边距。



元素的尺寸:

height 设置元素的高度。属性值：auto：默认。/px、cm 等单位定义高度。/百分比

width 设置元素的宽度属性值：auto：默认。/px、cm 等单位定义高度。/百分比



max-height 设置元素的最大高度。属性值：auto：默认。/px、cm 等单位定义高度。/百分比

max-width 设置元素的最大宽度。属性值：auto：默认。/px、cm 等单位定义高度。/百分比

这两个一般用于图片等的缩放限制



min-height 设置元素的最小高度。属性值：auto：默认。/px、cm 等单位定义高度。/百分比

min-width 设置元素的最小宽度。属性值：auto：默认。/px、cm 等单位定义高度。/百分比

当属性值用百分比时是相对于父元素的尺寸来说的。

最大最小宽高主要用于动态控制缩放等情况下，这里暂做了解。



padding 属性：元素的内边距:

padding-top 属性设置元素的上内边距（空间）。

padding-right 属性设置元素右内边距（空白）。

padding-bottom 属性设置元素的下内边距（底部空白）。

padding-left 属性设置元素左内边距（空白）。

padding 属性接受长度值或百分比值，但不允许使用负值。

padding * 同时设定四个边距

padding ** 分别设定上下、左右边距

padding *** 分别设定上、左右、下边距

padding **** 分别设定上、右、下、左边距

p标签有自动换行的效果



border属性：元素的边框，是围绕元素内容和内边距的一条或多条线。

border属性：

可以按顺序设置如下属性：

border-width

border-style

solid 定义实线。/dotted 定义点状边框/double 定义双线......

border-color

关于元素的边框后边课程还会详细讲解，暂时先简单了解。



```html
	*{
		padding: 0px;
		margin:0px;
        }    //用通配符取消浏览器默认边距
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

```html

```

margin 属性：元素的外边距:

围绕在元素边框的空白区域是外边距。设置外边距会在元素外创建额外的“空白”。

margin-top 属性设置元素的上外边距（空间）。

margin-right 属性设置元素外内边距（空白）。

margin-bottom 属性设置元素的下外边距（底部空白）。

margin-left 属性设置元素左外边距（空白）。

margin 属性接受长度值或百分比值，允许使用负值。

margin * 同时设定四个外边距

margin ** 分别设定上下、左右外边距

margin *** 分别设定上、左右、下外边距

margin **** 分别设定上、右、下、左外边距



```html
	#div1{
		margin-bottom: 30px;
	}
	#div2{
		margin-top: 50px;
        }    //两个div的外边距会重叠，div之间的距离是外边距大的那个
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

外边距的合并

外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。

合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。



溢出的处理

overflow 如果内容溢出了元素内容区域，是否对内容的边缘进行裁剪。//对x、y同时生效，建议用以下两个

overflow-x 如果内容溢出了元素内容区域，是否对内容的左/右边缘进行裁剪。

overflow-y 如果内容溢出了元素内容区域，是否对内容的上/下边缘进行裁剪。

visible 不裁剪内容，可能会显示在内容框之外。

hidden 裁剪内容 - 不提供滚动机制。

scroll 裁剪内容 - 提供滚动机制。

auto 如果溢出框，则应该提供滚动机制。

```html
white-space: nowrap;  //禁止换行
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



overflow-x: auto;





**6-29 css定位**

CSS定位的概念：

CSS 定位属性允许对元素进行定位改变其在页面的位置。

CSS 有三种基本的定位机制：普通流、浮动和绝对定位。

普通流中的元素的位置由元素在HTML中的位置决定。



元素定位的属性：

1. pos

   ition

   把元素放置到一个静态的、相对的、绝对的、或固定的位置中。

   1. static 默认值。没有定位。
   2. absolute 绝对定位，相对于(static 定位以外的第一个) 父元素进行定位。通过绝对定位，元素可以放置到页面上的任何位置。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。(注：static 定位以外的第一个父元素：相对与最接近的一个最有定位设置的父级对象进行绝对定位，如果对象的父级没有设置定位属性，则依据 body 对象左上角作为参考进行定位。)







​                且会占据<p>标签的位置：

​                    ![img](https://img-blog.csdn.net/20180423171252177?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xlYXJuX2luQ1NETg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

1. relative 相对定位，相对于其正常位置进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。
2. fixed 绝对定位，相对于浏览器窗口进行定位。元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。

滚动时div位置不变

1. 绝对定位和相对定位的区别

绝对定位对象可以层叠,相对定位的对象不可以

相对定位对象会占据它原来位置,绝对定位不会

1. top 定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。注：如果 "position" 属性的值为 "static"，那么设置 "top" 属性不会产生任何效果。

```html
top: -200px;   // 距上边距200px
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. right 定义了定位元素右外边距边界与其包含块右边界之间的偏移。注：如果 "position" 属性的值为 "static"，那么设置 "right" 属性不会产生任何效果。

2. bottom 定义了定位元素下外边距边界与其包含块下边界之间的偏移。注：如果 "position" 属性的值为 "static"，那么设置 "bottom" 属性不会产生任何效果。

3. left 定义了定位元素左外边距边界与其包含块左边界之间的偏移。注：如果 "position" 属性的值为 "static"，那么设置 "left" 属性不会产生任何效果。

4. clip 设置元素的形状。元素被剪入这个形状之中，然后显示出来。

   1. 语法 clip: rect(top, right, bottom, left);目前裁切形状只有矩形可以使用

   1. rect()需要设置四个值：top, right, bottom和left。他们之间需要用逗号隔开，而且rect()属性值和margin、padding一样的标准，遵循顺时针旋转的规则。
   2. 注意：clip属性只能在元素设置了“position:absolute”或者“position:fixed”属性起作用。
   3. auto：这是一个默认值，clip设置auto值和没有进行剪切是一样的效果;



![img](https://img-blog.csdn.net/20180423171507373?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xlYXJuX2luQ1NETg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

```html
img{
position: absolute; //auto等于没有裁剪
clip: rect(50px,315px,200px,20px);
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. vertical-align 设置元素的垂直对齐方式。

```html
display: inline-block;  //在一行显示
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

1. baseline 默认。元素放置在父元素的基线上。





​            基线是红色的线    

​            ![img](https://img-blog.csdn.net/20180423171531783?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xlYXJuX2luQ1NETg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

1. top 把元素的顶端与行中最高元素的顶端对齐

vertical-align: top;

1. middle 把此元素放置在父元素的中部。
2. bottom 把元素的底端与行中最低的元素的底端对齐。
3. 数值（像素）/百分比
4. text-top 把元素的顶端与父元素字体的顶端对齐
5. text-bottom 把元素的底端与父元素字体的底端对齐。
6. sub 垂直对齐文本的下标。
7. super 垂直对齐文本的上标

1. z-index 设置元素的堆叠顺序。
2. overflow 设置当元素的内容溢出其区域时发生的事情。
   1. ​    left 元素向左浮动。
   2. right 元素向右浮动。
   3. none 默认值。元素不浮动，并会显示在其在文本中出现的位置。
3. clear 浮动的清除：常用属性值 both/left/right/none

```html
clear: both;   //两种浮动都清除
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







**6-34 列表和表格**

表格有关的属性：

1. border-collapse 设置是否把表格边框合并为单一的边框.属性值：separate 默认值/collapse边框合并

```html
	table{
		/*默认值*/
		border-collapse: separate;
		/*合并边框*/
		border-collapse: collapse;
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. border-spacing 设置分隔单元格边框的距离。

```html
	table{
		border-collapse: separate;
		border-spacing: 8px;   //需要与 separate搭配使用
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. caption-side 设置表格标题的位置。属性值：top 默认值,在表格之上。bottom 在表格之下。
2. empty-cells 设置是否显示表格中的空单元格。属性值：hide/show默认
3. table-layout 设置显示宽度是否随内容拉伸。属性值：auto默认/fixed 列宽由表格宽度和列宽度设定。



列表的属性：

1. list-style 简写属性。用于把所有用于列表的属性设置于一个声明中。
2. list-style-type 设置列表项标志的类型。
   1. none无标记。/disc默认,实心圆。/circle 标记是空心圆。/square实心方块。/
   2. decimal 数字。/decimal-leading-zero 0开头的数字/lower-roman 小写罗马数字upper-roman 大写罗马数字/lower-alpha 小写英文字母/upper-alpha大写英文字母
   3. ......日文、拉丁文等其他符合，有兴趣自己查CSS手册。
3. list-style-position 设置列表项标志的位置。属性值：inside/outside(默认值)
4. list-style-image 将图象设置为列表项标志。属性值：URL 图像的路径。/none 默认。无图形被显示。

```html
list-style-image: url(../image/pen.jpg);
list-style: circle inside url(../image/pen.jpg);
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)





 ![img](https://img-blog.csdn.net/20180423171607538?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xlYXJuX2luQ1NETg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)