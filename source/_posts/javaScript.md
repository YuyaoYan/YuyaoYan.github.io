---
title: JavaScript基础
date: 2018-11-30 
tags: [fontend,JavaScript]
cover: /img/post-cover/1.jpg
---

#### 7-1

嵌入JavaScript代码的三种方式

1. 写在 script 标签中
2. 直接放在HTML标签中

```html
<script>
    document.write('djhfjdf');
</script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. 以外部文档的方式连接到当前HTML文档中



```html
<script type="text/javascript" src="7-1.js"></script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



注意事项：

1. 区分字母的大小写，Name和name是两个不同的标识符。
2. 空格和换行。这一点和CSS代码规则类似:多余的空格会被忽略，可以将一行代码分成多行写。
3. 分号作为一个语句的结束标志，分号之后是新语句的开始。虽然省略不写通常也是没有问题的，但还是建议大家写上。
4. 代码的注释：单行注释和多行注释。





#### 7-2

document.write()的常用操作

document.write('矩形的长为：'+b+',宽为：'+a+',面积为:'+c+'\n');

- 除了直接输出文字外，它还支持带有HTML标签的输出内容。
- 比如直接输出一个标题
- 比如在输出内容中加入br换行标签
- 比如直接输出列表项......
- ......以后再详细介绍，暂时先了解这么多.





alert()方法

- alert()方法会输出一个对话框，在以后的课程中我们会经常用它进行测试，务必先了解它的用法。
- 可以添加多个alert();他们会按照顺序依次执行。

var x=10;

alert(x);

可以验证变量的赋值是否正确



onclick事件的基本用法

- onclick()事件是最常用的事件之一，所谓事件可以简单理解为用户的操作。
- 为了后续课程的学习，你应该先掌握着个简单事件的基本用法





#### 7-3

常量

- 常量是从始至终不能被改变的数据。比如: 数字 123 可以是常量，字符串 "hello" 也是一个常量......
- 常量通常用来表示固定不变的量，比如圆周率，万有引力常量。





变量

- 变量的值是可以改变的，变量可以看做是存储数据的容器。比如一个瓶子，它既可以装入酱油、醋；也可以装入茅台和二锅头......
- 在 JavaScript 中创建变量通常称为“声明”变量，使用关键字 var来声明变量。
- 向变量赋值，使用等号;可以在声明变量时对其赋值，也可以先声明后赋值。
- 可以在一条语句中声明很多变量。该语句以 var 开头，并使用逗号分隔变量即可





数据类型

- 可以使用typeof(变量名)查询数据类型
- 数据类型包括:字符串、数字、布尔、数组、对象、Null、Undefined
- 数字 number: JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：
- 字符串 string:字符串 是存储字符的变量。
- 布尔 boolen:只能有两个值：true 或 false。
- 数组 array:
- null 空值:可以通过将变量的值设置为 null 来清空变量。
- object: 对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔。
- Undefined 这个值表示变量不含有值或未声明。





温馨提示：注意事项

- 在一个HTML文档使用script标签嵌入多个JS语句的时候，这几个语句之间是相通的,或者说是有关联的。
- 命名规范(包括函数名，变量等):
- 必须以字母、下划线或者美元符号开始，不能使用特殊符号。
- 命名不能是系统的关键字：比如new ,if,class......
- 区分大小写
- 命名最好用有意义的名称。比如说name,people......





#### 7-4数据类型

​       数据类型包括:字符串、数字、布尔、数组、对象、Null、Undefined

​       关于数据类型的分类，不同书籍的分类方法有所不同，有的划分为复杂数据类型和简单数据类型，也有的划分为原始数据类型和复合数据类型；

​       有的书籍将函数作为一种特殊的数据类型，有的认为函数不算是数据类型；

​       本节课程的讲解将重点介绍数值和字符串，要求大家掌握；布尔型的演示涉及的后边章节内容，暂时要求了解；至于数组和对象，暂时先做简要了解，知道即可，将在后续章节做进一步的深入学习。



typeof运算符 

typeof运算符可以查询数据类型

其返回可能值有:undefined,boolean,number,string、object以及function.





字符串型数据String：字符串是存储字符的变量。

常量字符串：如 "JavaScript",'HTML5' 

变量字符串：如：var text="HTML5视频教程"

可以使用"+"进行字符串的连接。

在JavaScript 中，字符串使用单引号或者双引号来起始或者结束。那么如何输出单引号或者双引号呢？就要用到转义字符

JavaScript中常用的转义字符

换行符：\n

回车符：\r

退格符:\b

反斜杠:\\

双引号:\"

......

温馨提示：部分转义字符在输出为HTML文档流时不发生作用。





数值型数据Number：

1. JavaScript 只有一种数字类型。数字可以带小数点，也可以不带。
2. 浮点数值的最高精度是17位小数，但是在进行算术计算时其精度远远不如整数。例如，0.1加0.2的结果不是0.3， 而是0.30000000000000004。这个舍入误差会导致无法测试特定的浮点数值。
3. 极大或极小的数字可以通过科学（指数）计数法来书写：3e4

3.14e2就是3.14*100=314

1. 数字可以写成十进制、八进制、十六进制。
2. 八进制在js中表示是第一位一定要是0，后面就是八进制字数序列（0~7）
3. 十六进制字面量前两位必须是0x,后面跟十六进制数字（0~9及A~F）。字母A~F不区分大小写。

温馨提示：科学（指数）计数法、八进制、十六进制表示的数字在输出时统统会转换成十进制。





布尔型数据Boolen:

1. 布尔型数据boolen:只能有两个值：true 或 false。

var m=3;

var n=5;

alert(m>n);   //  function alert(message?: any): void  弹出框显示为：false



1. 将各种类型的值转化成Boolean类型的规则如下：
   1. Number:任意非0的数值为true,0值和NaN为"false"。
   2. String:所有的非空字符串转化为 true; ""（空字符串）转化成false

if("..."){

alert("布尔值为真")

}else{

alert("布尔值为假")

}

1. Object的任何对象都会转化为 true;
2. 在javascript中，只要逻辑表达式不返回undefined不返回null，就都是真的。



Undefined

1. 这是一个很有意思的数据类型，因为它的值只有一个，那就是undefined。

var m;

alert(typeof  m)

1. 在申明变量时如果没有将变量赋值的话这个变量也是属于Undefined类型的。。
2. 如果一个变量没有申明就直接去访问解释器会报错误信息，但是这样的变量如果使用typeof返回的结果也是"undefined"。





Null:空值 

Null也是一个只有一个值得数据类型，它的值就是null，任何变量只要给其赋值为null的话这个变量的数据类型就是Null类型。

可以通过将变量的值设置为 null 来清空变量。





对象Object:

在javascript中，所有的对象都继承自Object对象（数组是特殊的对象，所以数据类型也是object）。

对象对于初学者来说不是很容易理解，在后续课程中再详细讲解，这里大家先记住有这种数据类型即可。

// 定义对象，通过.来访问

var person={name:'Yoyo',age:'24',id:'17127907',VIP:'会员'}

alert(person.age)





数组Array:

可以通过"."来访问数组的元素。

数组元素的顺序从0开始



实例1：

```javascript
//鸡兔同笼
<script>
    var head=35;
    var foot=94;
    varchicken=head-(foot-2*head)/2;
    var rabbit=(foot-2*head)/2;
    document.write('头的数量为:'+head+'<br>');
    document.write('脚的数量为:'+foot+'<br>'); 
</script>
<input type="button" name=""value="鸡的数量"onclick="document.write('计算鸡的数量为：'+chicken)"/>
<input type="button" name=""value="兔的数量"onclick="alert('计算兔的数量为：'+rabbit)"/>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







#### 7-10 运算符

基本概念

1. 表达式：由常量/变量和运算符组成的短语；
2. 操作数：表达式中的常量和变量成为操作数；
3. 运算符：表达式中起运算作用的符合成为运算符；
4. 单目运算符：只能带一个操作数的成为单目运算符；(也叫一元运算符)
5. 多目运算符：带多个操作数的成为多目运算符；





用于字符串的 + 运算符

- \+ 运算符用于把文本值或字符串变量加起来（连接起来）。
- 要想在两个字符串之间增加空格，需要把空格插入一个字符串之中：
- 如果把数字与字符串相加，结果将成为字符串。





赋值运算符：

- 赋值运算符用于给 JavaScript 变量赋值。
- =: x=y
- += x+=y 等价于 x=x+y
- -= x-=y 等价于 x=x-y
- *= x*=y 等价于 x=x*y
- /= x/=y 等价于 x=x/y
- %= x%=y 等价于 x=x%y





算术运算符

- 加减乘除：+ - * /
- 取模运算符：%
- 正负运算符：+ -
- 递增递减运算符：++ --:使数字递增/递减1(注意前置和后置的区别)
- 若没有赋值前置和后置，同。
- 若有赋值:前置则先计算递增/减后赋值，后置则相反。





比较运算符

- 比较运算符是比较两个数的大小的运算符，返回的是一个布尔值。
- 相等运算符 == ：判断两个操作数是否相等。不同的数据类型会自动转换为相等的数据类型再做比较。
- 等同运算符=== ：全等（值和类型），严格意义的相等，两个操作数的值和他们的类型必须完全一致。
- 不等于：!=
- 不等同运算符： !==
- 大于：>
- 小于：<
- 大于或等于：>=
- 小于或等于：<=
- 若一个是数值字符串，一个是数值，字符串会自动转换成数值进行比较。
- 若两个都是字符串，则比较首个数字的大小。
- 字母字符串会转换成对应的ASCII码(较少用到，不做讲解，知道即可)
- 布尔值的false和true会转换成0和1





逻辑运算符

- 逻辑运算符用于测定变量或值之间的逻辑。
- && and(与)
- || or(或)
- ! not(非)





条件运算符

- 根据条件在两个语句中执行其中的一个，使用符号 ？：语法如下：
- 条件表达式？语句1：语句2
- 参数说明：
- 条件表达式，结果会被作为布尔值处理
- 语句1：如果条件表达式返回true则执行
- 语句2：如果条件表达式返回false则执行





运算符优先级

运算符优先级描述了在计算表达式时执行运算的顺序。先执行具有较高优先级的运算，然后执行较低优先级的运算。例如，先执行相乘，再执行相加。

- 运算符比较多，可以合理使用()来改变表达式的优先级。
- ()的用法和数学中的()用法相同,()内的会优先计算。



#### 7-15控制语句

基本概念

- 单行语句
- 复合语句
- 代码块
- 复合语句也会被当做一条语句来处理





if选择语句

条件语句用于基于不同的条件来执行不同的动作。



- if() 语句 - 只有当指定条件为 true 时，使用该语句来执行代码
- if()...else 语句 - 当条件为 true 时执行代码，当条件为 false 时执行其他代码
- if()...else if()....else 语句 - 使用该语句来选择多个代码块之一来执行
- if语句()中的表达式会自动转换成布尔值。





switch多条件选择语句

使用 switch语句来选择要执行的多个代码块之一。



语法：

switch(n)

{

case 1:

执行代码块 1

break;

case 2:

执行代码块 2

break;

default:

n 与 case 1 和 case 2不同时执行的代码

}



工作原理：首先设置表达式n（通常是一个变量）。

随后表达式的值会与结构中的每个 case的值做比较。

如果存在匹配，则与该 case关联的代码块会被执行。

请使用 break 来阻止代码自动地向下一个case 运行。

default关键词来规定匹配不存在时做的事情：





for 循环语句

在编程中有些指令需要执行很多遍，这时候就要用到循环语句。



for 循环的语法：

for (语句 1; 语句 2; 语句 3)

{

被执行的代码块

}

语句 1 在循环（代码块）开始前执行

语句 2定义运行循环（代码块）的条件,如果语句 2 返回 true，则循环再次开始，如果返回 false，则循环将结束。

语句 3 在循环（代码块）已被执行之后执行

语句 1 是可选的，也就是说不使用语句 1也可以。

如果您省略了语句 2，那么必须在循环内提供break。否则循环就无法停下来。这样有可能令浏览器崩溃。

语句 3 也是可选的。



while循环

while循环在执行前测试一个条件，如果条件成立进入循环。

while 循环的语法：

while(条表达式)

{

语句组

}





do-while循环

while循环在执行前测试一个条件，而do-while循环先执行循环，然后再测试条件成立与否。

while 循环的语法：

do

{

语句组

}

while(条表达式)





break和continue跳转语句

break将直接跳出并结束当前循环结构。

continue用于跳过循环中的一个迭代。

continue语句只能用在循环中；break只能用在循环或 switch 中。





其他控制语句

for/in - 循环遍历对象的属性，with、return语句等





九九乘法表

```html
<script>
    for(var i=1;i<=7;i++){
        for(var j=1;j<=i;j++){
        var str=i+"x"+j+"="+i*j+" ";
        document.write(str);
        }
        document.write("<br>");
    }
</script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







math.floor(x) //返回小于参数x的最大整数，即向下取整



#### 7-22 函数

基本概念

函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块。

JavaScript 函数语法:函数就是包裹在花括号中的代码块：

function 函数名()

{

这里是要执行的代码

}





函数的声明和调用：

使用了关键词 function来声明函数

关键词function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。

函数本身不会自动运行，只有当调用该函数时，才会执行函数内的代码。

函数可以通过其名字加上括号中的参数进行调用

可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用。

在调用函数时，您可以向其传递值，这些值被称为参数。带有参数的函数也被称为有参函数。





带有返回值的函数:

有时，我们会希望函数将值返回调用它的地方。通过使用 return 语句就可以实现。

在使用return 语句时，函数会停止执行，并返回指定的值。

function hs(){

return('返回值');

}

hs();

alert('可以直接对返回值操作，比如输出它：'+hs());

可以将返回值赋值给一个变量，然后对变量进行操作

当函数遇到第一个return后将终止执行函数后边的语句，直接跳出函数

var a=sum(3,5);





arguments 对象:

在函数代码中，使用特殊对象 arguments存储函数调用传递给该函数的所以参数。

还可以用arguments 对象检测函数的参数个数，引用属性 arguments.length 即可。

arguments [0]表示函数的第一个参数，arguments [1]表示函数的第二个参数......

通过arguments可以动态的添加参数。





实例三：函数在canvas中的应用

```html
<body onload="draw()">
    <canvas id="myCanvas" width="600px" height="300px" style="border:1pxsolid #c3c3c3;"></canvas>
    <script>
    function draw(){
        var c=document.getElementById("myCanvas");
        var cxt=c.getContext("2d");
        for(var i=0;i<12;i++){
            for(var j=0;j<24;j++){
                cxt.fillStyle='rgb(240,'+Math.floor(255-11.5*i)+','+Math.floor(255-11.5*j)+')';
                cxt.beginPath();
                cxt.arc(12.5+i*25,12.5+j*25,10,0,Math.PI*2,true);
                cxt.closePath();
                cxt.fill();
            }
        }
    }
</script>
</body>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



#### 7-27 对象和数组

对象:Object 

1. JavaScript 中的所有事物都是对象：字符串、数值、数组、函数...
2. 对象是属性的集合，每个属性都有名字和值，对象可以通过属性的名字存取属性的值。
3. 对象的属性既可以存放基本数据类型也可以存放其他对象的引用值或者函数的引用值，如果存储的是函数的的引用值则该属性称为方法
4. 对象可以看做带有属性和方法的特殊数据类型。
5. 对象包含两个基本要素：属性-值，也称作键-值/名-值;当属性值为方法时也称作：属性(字段)和方法(函数)
6. 对象的创建方法
   1. 通过new运算符创建
   2. new关键字可以省略
   3. 属性可以用引号包含也可以不用

```html
<script>
    // 先创建一个空的对象再赋值
    var peo=new Object();
    peo.name='songjiang';
    peo.sex='man';
    alert(peo.name);
</script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



```html
<script>
    // 先创建一个空的对象再赋值
    var peo={};
    peo.name='songjiang';
    peo.sex='man';
    alert(peo.name);
</script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



```html
<script>
    //直接对创建的对象赋值
    var peo={
    name:'songjiang'，
    sex:'male'
    }
    alert(peo.name);
</script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







1. 可以用点符号访问对象属性值也可以通过数组的方式，即用["属性名称"]

alert(peo['name']);



1. 可以使用delete运算符删除对象的属性。

delete peo.name;



​       //属性值为函数：

function say(){

return('大师兄');

}

var people={

sa:say

}

alert(people.sa());



数组:Array



数组的声明(创建)方法:

1. new关键字创建空数组
2. new关键字创建包含元素的数组
3. new关键字创建指定元素个数的数组

```javascript
<script>
    var arr1=new Array();
    var arr2=new Array('apple','banana','orange');
    var arr3=new Array(4);
    alert(arr1);
</script>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. 也可以使用[]直接创建数组



var arr1=[];

var arr2=['apple','banana','orange',1];

var arr3=[];

arr3[0]='hha';

arr3[1]='xx';

alert(arr3[0]);

1. 可以使用length属性获取数组的长度;并且可以给一个数组赋值

alert(arr2.length);

arr3.length=6;          //给数组赋值长度为6



数组元素的基本操作

程序运行时通常需要读取数组中的数据，有时候需要对数据进行修改。

1. 读取数据：可以使用索引查询获取数组元素和添加数组元素
2. 添加数据：使用push方法将新元素添加到数组尾部.

var fruit=new Array('苹果','putao');

fruit.push('taozi');

document.write(fruit);

1. 删除数据：可以使用delete运算符删除指定的元素。

delete fruit[0];

1. 删除末尾元素(更新数据)pop()方法：该方法会返回删除的元素。

fruit.pop();

document.write(fruit.pop());   //打印该函数的返回值，即已删除的元素

1. 删除顶端的元素 shift方法：
2. 在数组顶端添加元素 unshift方法：返回值为新数组的长度，但不建议使用，IE会出错。
3. 字符转换：toString方法将数组表示为字符串。



1. join方法输出数组元素。(输出结果会转换成字符串)

//默认输出时，每个元素会用逗号隔开，jion()可以改变输出时的间隔方式

var fruit=newArray('苹果','putao','fdf','fddgdf');

document.write(fruit.join('-')+'<br>');

1. 数组逆序reverse：颠倒数组元素的顺序;返回值为逆序后的新数组。

fruit.reverse();

1. 数组排序 sort：



1. 语法 数组名.sort(sortfunction)

//两位数以上的数组元素会出错

1. sortfunction若省略，默认为从按照ASII字符顺序进行升序排列
2. sortfunction必须返回：正值、零、负值三者之一。赋值表示第一个值大于第二个值，负值反之，零则相等。

```javascript
var fruit=new Array('1','36','21','88');
document.write(fruit+'<br>');
fruit.sort(sortFunction);
document.write(fruit+'<br>');
function sortFunction(ar1,ar2){
    if(ar1>ar2){
        return -1;
    }else if(ar1<ar2){
        return 1;
    }else{
        return 0;
    }
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. 扩充数组 concat:将多个数组的元素合并为一个新的数组。





```javascript
var fruit=fruit1.concat(fruit2)
document.write(fruit+'<br>')
//参数也可以是元素：
var fruit=fruit1.concat('apples')
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

splice方法：删除、替换、插入元素 



1. 1. 会更改原数组
   2. 第一参数为起始位置索引
   3. 第二参数为切取元素个数
   4. 第三个参数为插入元素，可选项









切取数组的一段元素 slice：

```html
var fruit1=new Array('苹果','苹果','苹果','苹果');
document.write(fruit1+'</br>');
var fruit2=fruit1.splice(1,2,'葡萄','梨');
//varfruit2=fruit1.splice(1,2);
document.write(fruit1+'</br>');
document.write(fruit2+'</br>');
//splice的返回值是被替换的元素，返回类型是object，即返回的两个元素新构成的数组的类型
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



1. 1. 切取部分作为新数组返回，不会对原数组改变。
   2. 第一参数为起始位置索引
   3. 第二参数为结束位置索引，注意区分splice
   4. 若省略第二个参数则直接切取到结尾



```javascript
var fruit1=new Array('苹果1','苹果2','苹果3','苹果4','苹果5','苹果6','苹果7','苹果8');
document.write(fruit1+'</br>');
var fruit2=fruit1.slice(1,4);
document.write(fruit1+'</br>');
document.write(fruit2+'</br>');
//切取1-4，不包括4.slice不对原参数操作，返回切取出来的值；但splice对原数组进行操作，返回切取的值
 
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







in 运算符和for in循环语句

- in 运算符用来检测对象中是否具有某一特定属性，通常用于遍历集合中的所有元素。
- 通常我们使用for/in 语句循环遍历对象的属性，在数组中可以遍历数组中的所有元素。

//for in循环在对象中的应用：

```javascript
var person={name:"张三",age:25,ID:12345}
for (x in person){
    document.write('<li>'+person[x]+'<br>') //输出属性值
    document.write('<li>'+x+'<br>') //输出属性
}
 
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



#### 阶段练习



n!



```javascript
var n=4;
function rrr(n){
    if(n==1){
        return 2;
    }else
        return rrr(n-1)*n;
    }
document.write(rrr(n));
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

回文



Math.floor()可对浮点数取整



```css

```

var i,a,b,c,d; var ss=new Array(); function aa(){     for(i=10;i<=9999;i++){         d=i%10;         c=Math.floor((i/10)%10);         b=Math.floor((i/100)%10);         a=Math.floor((i/1000)%10);

​        if((a==d&&b==c&&a!=0)||(a==0&&b==d)||(a==0&&b==0&&c==d)){             ss.push(i);         }     } } aa(); alert(ss.length); document.write(ss+'<br>');



#### 7-35 时间和日期



基本概念

Date是JavaScript的内置对象，系统在Date对象中封装了与日期和时间相关的属性和方法。

Date使用UTC1970年1月1日0时开始经过的毫秒数来存储时间。

GMT 格林尼治时间

UTC 国际协调时间





创建Date对象四种方法：

- var date= new Date();
  - 无参数的情况下返回值为当前时间。
  - 不同浏览器显示的时间格式会有细微差异
- var date = new Date(milliseconds);
- var date = new Date(dateString);
- var date = new Date(year, month, day, hours, minutes, seconds, milliseconds);

```javascript
var date1=new Date();
var date2=new Date(21212645615312);
var date3=new Date(2012,1,24);
var date4=new Date(2012,1,24,10,10,10);
 
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



时间相关的两个方法(这两种方法了解一下就可以了)：

- Date.parse()返回1970年1月1日午夜到指定日期（字符串）的毫秒数。
- Date.parse()参数支持的时间格式如下：

1/24/2016;

January 24,2016；

SunJan 24 2016 10:10:10 GMT+0800

格式不正确会返回NaN

- Date.UTC()根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。
- Date.UTC()参数支持的时间格式如下：

2016,1(前两个参数是必须的);

2016,1,24,10,10,10

数值含义为年/月/日/时/分/秒；格式不正确会返回NaN

月份和日期是从0开始

注意UTC时间和时区的换算，如东八区和标准时间是八小时时差





Date实例相关的字符串表示方法(了解即可)：

- toSting()获取Date实例的字符串表示
- toDateSting()获取Dater的日期部分字符串表示
- toTimeSting()获取Dater的时间部分字符串表示
- toLocaleString() 据本地时间格式，把 Date 对象转换为字符串。
- toLocaleDateString() 根据本地时间格式，把 Date 对象的日期部分转换为字符串。
- toLocaleTimeString() 根据本地时间格式，把 Date 对象的时间部分转换为字符串。
- valueOf():转换为毫秒数





Date 对象方法

通过使用针对日期对象的方法，我们可以很容易地对日期进行操作。重点掌握蓝色字体的内容，其他了解即可。

- getDate() 从 Date 对象返回一个月中的某一天 (1 ~ 31)。
- getDay() 从 Date 对象返回一周中的某一天 (0 ~ 6)。
- getFullYear() 从 Date 对象以四位数字返回年份。
- getHours() 返回 Date 对象的小时 (0 ~ 23)。
- getMilliseconds() 返回 Date 对象的毫秒(0 ~ 999)。
- getMinutes() 返回 Date 对象的分钟 (0 ~ 59)。
- getMonth() 从 Date 对象返回月份 (0 ~ 11)。
- getSeconds() 返回 Date 对象的秒数 (0 ~ 59)。
- getTime() 返回 1970 年 1 月 1 日至今的毫秒数。

- getTimezoneOffset() 返回本地时间与格林威治标准时间 (GMT) 的分钟差
- getUTCDate() 根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。
- getUTCDay() 根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。
- getUTCFullYear() 根据世界时从 Date 对象返回四位数的年份。
- getUTCHours() 根据世界时返回 Date 对象的小时 (0 ~ 23)。
- getUTCMilliseconds() 根据世界时返回 Date 对象的毫秒(0 ~ 999)。
- getUTCMinutes() 根据世界时返回 Date 对象的分钟 (0 ~ 59)。
- getUTCMonth() 根据世界时从 Date 对象返回月份 (0 ~ 11)。
- getUTCSeconds() 根据世界时返回 Date 对象的秒钟 (0 ~ 59)。
- parse() 返回1970年1月1日午夜到指定日期（字符串）的毫秒数。

- setDate() 设置 Date 对象中月的某一天 (1 ~ 31)。
- setFullYear() 设置 Date 对象中的年份（四位数字）。
- setHours() 设置 Date 对象中的小时 (0 ~ 23)。
- setMilliseconds() 设置 Date 对象中的毫秒 (0 ~ 999)。
- setMinutes() 设置 Date 对象中的分钟 (0 ~ 59)。
- setMonth() 设置 Date 对象中月份 (0 ~ 11)。
- setSeconds() 设置 Date 对象中的秒钟 (0 ~ 59)。
- setTime() setTime() 方法以毫秒设置 Date 对象。

- setUTCDate() 根据世界时设置 Date 对象中月份的一天 (1 ~ 31)。
- setUTCFullYear() 根据世界时设置 Date 对象中的年份（四位数字）。
- setUTCHours() 根据世界时设置 Date 对象中的小时 (0 ~ 23)。
- setUTCMilliseconds() 根据世界时设置 Date 对象中的毫秒 (0 ~ 999)。
- setUTCMinutes() 根据世界时设置 Date 对象中的分钟 (0 ~ 59)。
- setUTCMonth() 根据世界时设置 Date 对象中的月份 (0 ~ 11)。
- setUTCSeconds() setUTCSeconds() 方法用于根据世界时 (UTC) 设置指定时间的秒字段。
- toDateString() 把 Date 对象的日期部分转换为字符串。
- toGMTString() 已废弃。请使用 toUTCString() 方法代替。
- toISOString() 使用 ISO 标准返回字符串的日期格式。
- toJSON() 以 JSON 数据格式返回日期字符串。
- toLocaleDateString() 根据本地时间格式，把 Date 对象的日期部分转换为字符串。
- toLocaleTimeString() 根据本地时间格式，把 Date 对象的时间部分转换为字符串。
- toLocaleString() 据本地时间格式，把 Date 对象转换为字符串。
- toString() 把 Date 对象转换为字符串。
- toTimeString() 把 Date 对象的时间部分转换为字符串。
- toUTCString() 根据世界时，把 Date 对象转换为字符串。
- UTC() 根据世界时返回 1970 年 1 月 1 日 到指定日期的毫秒数。
- valueOf() 返回 Date 对象的原始值。





#### 7-38 Math对象

Math 对象

Math 对象用于执行数学任务。

Math 对象并不像 Date 和 String 那样是对象的类，因此没有构造函数 Math()。





算数值

JavaScript提供 8 种可被 Math 对象访问的算数值：

- Math.PI 返回圆周率（约等于3.14159）。
- Math.E 返回算术常量 e，即自然对数的底数（约等于2.718）。
- Math.SQRT2 返回 2 的平方根（约等于 1.414）。
- Math.SQRT1_2 返回返回 1/2 的平方根（约等于 0.707）。
- Math.LN2 返回 2 的自然对数（约等于0.693）。
- Math.LN10 返回 10 的自然对数（约等于2.302）。
- Math.LOG2E 返回以 2 为底的 e 的对数（约等于 1.443）。
- Math.LOG10E 返回以 10 为底的 e 的对数（约等于0.434）。





数值取整

- ceil(x) 对数进行上舍入。
- floor(x) 对数进行下舍入。
- round(x) 把数四舍五入为最接近的整数。





随机数

- random() 返回 0 ~ 1 之间的随机数。

注意并不包括0和1

```javascript
//返回1-10,包括10
for(var i=0;i<10;i++){
    document.write(Math.floor(Math.random()*10+1)+"<br>");
}
//返回2-10,包括10
for(var i=0;i<10;i++){
    document.write(Math.floor(Math.random()*9+2)+"<br>");
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







例：

```javascript
function selec(low,high){
    var ch=high-low+1;
    return Math.floor(Math.random()*ch+low);
}
    for(var i=0;i<10;i++){
        document.write(selec(49,88)+"<br>");
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)







三角函数

- cos(x) 返回数的余弦。





alert(Math.cos(Math.PI/3));    //cos(这里是弧度)



```javascript
alert(Math.cos(Math.PI/3));    //cos(这里是弧度)
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



- acos(x) 返回 x 的反余弦值。
- sin(x) 返回数的正弦。
- asin(x) 返回 x 的反正弦值。
- tan(x) 返回角的正切。
- atan(x) 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。







其他方法

- max(x,y) 返回 x 和 y 中的最高值。

- min(x,y) 返回 x 和 y 中的最低值。

  ```javascript
  var n=Math.min(1,8,6,3);
  ```

  ![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

```html

```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)



- abs(x) 返回 x 的绝对值。
- atan2(y,x) 返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。
- exp(x) 返回 e 的指数。
- log(x) 返回数的自然对数（底为e）。
- pow(x,y) 返回 x 的 y 次幂。
- valueOf() 返回 Math 对象的原始值。





#### 7-40  字符串对象

字符串对象

1. 字符串是非常重要的数据类型，除了基本字符串外，JavaScript还提供了字符串的引用类型--字符串对象。
2. 字符串对象提供了字符串检索、替换、连接等方法...
3. 可以通过new 关键字创建字符串对象

var str=new String()

1. length 属性返回字符串的长度(字符数)。





字符串与数字的转换

1. toString() 返回字符串。可以将数值转换成字符串。
2. 如果需要获取数值的二进制、八进制、十六进制的字符串表示，则可以给toString()传递一个表示进制的的整数
3. parseInt()函数可以将字符串转换成整数
4. parseFloat()函数可以将字符串转换浮点数
5. Number()函数可以将任意类型的值转换数值。





字符串对象的常用方法

1. charAt() 返回在指定位置的字符。
2. charCodeAt() 返回在指定的位置的字符的 Unicode 编码。
3. concat() 连接字符串。
4. slice(n,m) 提取字符串n到m之间的片断(不包括m位置的字符串)，并在新的字符串中返回被提取的部分。
5. substring() 提取字符串中两个指定的索引号之间的字符。大多数情况和上一个作用相同，当参数为负值时会有不同，但这种情况较少用，不做讨论，有兴趣的话自己测试或查下资料
6. substr(n,m) 从起始索引号提取字符串中指定数目的字符。
7. split() 把字符串分割为字符串数组。
8. indexOf() 检索字符串,返回某个指定的字符串值在字符串中首次出现的位置。注意，如果查找不到会返回 -1







lastIndexOf() 从后向前搜索字符串。

```html
var str1="hello";
var s1=str1.indexOf('a')
alert(s1)
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

lastIndexOf() 从后向前搜索字符串。



1. toLowerCase() 把字符串转换为小写。
2. toUpperCase() 把字符串转换为大写。
3. match() 找到一个或多个正则表达式的匹配。(正则表达式后续课程会讲)



该方法会返回一个数组，数组中包含了所有符合条件的文本。无则返回null

1. replace() 替换与正则表达式匹配的子串，并返回替换后的字符串，注意原字符串不会改变
2. search() 检索与正则表达式相匹配的值。查找与参数模式相匹配的文本，并返回该文本的位置。若无则返回-1(indexOf()会返回-1).与indexOf()相似。
3. split() 把字符串分割为字符串数组。
4. ......

需要注意的是，JavaScript 的字符串是不可变的（immutable），String 类定义的方法都不能改变字符串的内容。像String.toUpperCase() 这样的方法，返回的是全新的字符串，而不是修改原始字符串。





#### 阶段练习

随机背景颜色：

```html
<script>
    var colors=['red','blue','yellow','purple','orange']
    function acolor(){
    var c=Math.floor(Math.random()*5)
    document.bgColor=colors[c]
}
</script>
<input type="button"value="更换背景颜色"onclick="acolor()">
 
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

