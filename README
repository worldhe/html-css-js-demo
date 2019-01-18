CSS文档流

- 文档流处在网页的最底层，它表示的是一个页面中的位置，我们所创建的元素默认都处在文档流中。
- 元素在文档流中的特点
  1. 块元素
     块元素在文档流中会独占一行，块元素会自上而下排列。
     块元素在文档流中默认宽度是父元素100%。
     块元素在文档流中默认高度被内容撑开。
  2. 行内元素（内联元素）
     行内元素在文档流中只占自身的大小，会默认从左向右排列，如果一行中不足以容纳所有行内元素，会自动换到下一行。
     行内元素在文档流中默认宽度和高度被内容撑开。
  3. 一旦元素脱离文档流，就都变成块元素了，但是宽度和高度是被内容撑开的，也可以设置宽度和高度。

CSS浮动

使用float来使元素浮动，从而脱离文档流（气球）。

none：默认值，元素默认在文档流中排列。

left：元素会立即脱离文档流，向页面的左侧浮动。

right：元素会立即脱离文档流，向页面的右侧浮动。

当一个元素设置浮动以后（float属性是一个非none的值），元素会立即脱离文档流，元素脱离文档流以后，它下边的元素会立即向上移动。

元素浮动以后，会尽量向页面的左上或右上漂浮，直到遇到父元素的边框，或其它的浮动元素停止。

如果浮动元素上边是一个没有浮动的块儿元素，则浮动元素不会超过块元素（上面的块元素就相当于一堵墙）。

浮动的元素不会盖住文字，文字会自动环绕在浮动元素的周围。

CSS定位

当开启了定位（position属性值是一个非static的值）时，可以通过left、right、top、bottom四个属性来设置元素的偏移量

left：元素相对于其定位位置的左侧偏移量。

right：元素相对于其定位位置的右侧偏移量。

top：元素相对于其定位位置的上面的偏移量。

bottom：元素相对于定位位置的下面的偏移量。

通常偏移量只需要使用两个就可以对元素进行定位，即

left、top

left、bottom

right、top

right、bottom

- 相对定位
  当元素的position属性设置为relative时，则开启了元素的相对定位。
  1. 当开启了相对定位以后，而不设置偏移量时，元素不会发生任何变化。
  2. 相对定位是相对于元素在文档流中原来的位置进行定位。
  3. 相对定位的元素不会脱离文档流。
  4. 相对定位会使元素提升一个层级。
  5. 相对定位不会改变元素的性质，行内元素还是行内元素，块元素还是块元素。
- 绝对定位
  当元素的position属性设置为absolute时，则开启了元素的绝对定位。
  1. 开启了绝对定位以后，会使元素脱离原来的文档流。
  2. 开启绝对定位以后，而不设置偏移量时，元素位置不会发生任何变化。
  3. 绝对定位是相当于离他最近的开启了典韦的祖先元素进行定位的（一般情况，开启了子元素的绝对定位都会同时开启父元素的相对定位），如果所有的祖先元素都没有开启定位，则会相对于浏览器窗口进行定位。
  4. 绝对定位会使元素提升一个层级。
  5. 绝对定位会改变元素的性质，行内元素变成块儿级元素，块元素的宽度和高度默认都被内容撑开。
- 固定定位
  当元素的position属性设置为fixed，则开启了元素的固定定位。
  1. 固定定位也是一种绝对定位，它的大部分特点都和绝对定位相同。不同的是，固定定位永远都是相对于浏览器窗口进行定位。
  2. 固定定位会固定在浏览器窗口的某个位置，不会随滚动条滚动。
  3. IE6不支持固定定位（如果想要兼容，就要使用js）。
- 层级问题
  1. 如果定位元素的层级是一样的，下边的元素会覆盖上边的（指html文档的上下边）。
  2. 通过z-index指定属性可以用来设置元素的层级。
  3. z-index指定一个正整数作为值，该值将会作为当前元素的层级，层级越高，越优先显示。
  4. 对于没有开启定位的元素不能使用z-index。
  5. 父元素的层级再高，也不会盖住子元素。
  6. 层级问题出现覆盖以后，设置元素透明背景
     - opacity可以用来设置元素的背景透明，它是一个0-1之间的值，0：绝对透明，1：绝对不透明。
     - opacity属性在IE8及一下的浏览器中不支持，可以使用alpha（opacity=透明度）替换，他是一个0-100之间的值，0：绝对透明，100：绝对不透明。
     - IE6支持opacity属性。

JS输出

- 警告框
  window.alert('hello world');
  在浏览器网页上会出现警告框。
  window可以省略,即alert('hello world');
  括号中的内容用单引号，即'hello world'。
- 在HTML文档中直接输出
  document.write('hello world');
- 在HTML指定元素中输出（要获取指定元素eg：getElementById("")）
  <p id="one"></p>
  <script type="text/javascript">
  document.getElementById("one").innerHTML = 'helloworld';
  </script>
- 写到浏览器控制台
  console.log('hello world');
  打开浏览器控制台即可找到。

JS语法

var可以声明各种数据类型

- 字符串
  var s = "John";		//s为字符串
  var carname = "LEXUS";
  var carname = 'AUDI';
- 数字
  var n = 5;		//n是数字
  var n = 20.00;
  var n = 20;
- 布尔
  var x = true;
  var y = false;
- 数组（定义数组三种方式）
  1. var cars = new Array();
     cars[0] = "Accord";
     cars[1] = "BMW";
  2. var cars = new Array("Accord","BMW");
  3. var cars = ["Accord","BMW"];
     cars.length可以获取数组的长度。
- 对象
  var person = {firstname:"John", lastname:"Doe",id=5566};
- 空Null
  var animal = null;		//animal为null
- 未定义Undefine
  var n;		//n未定义
- 赋值运算符
  var a = 1;
  a += 3; ==>a = 1+3;
- 算数运算符
  var a = 2;
  a = a *3;
- 字符串+运算符
  var a = 'hello';
  var b = 'world';
  var d = a + b;
- 比较与逻辑运算符
  1. 小于<
  2. 大于>
  3. 等于==（1 == '1'）不严格相等
  4. 绝对等于===（值和类型都相等）
  5. 不等于!=
  6. &&  and
  7. ||  or
- 条件语句
  1. if else if
  2. switch case break default
- 循环语句
  1. for
  2. while
- 代码块（函数,可重复使用，有两种定义方式）
  1. function a(){
     }
  2. var a = function(){
     }
  定义了一个方法a，a中可以写一些业务逻辑，通过调用a方法，去执行。
  还可以使用return关键字。
- 获得元素
  1. document.getElementById("");
  2. document.getElementsByTagName();
  3. document.getElementsByClassName();
- DOM事件（三种写法）
  1. <h1 onclick="this.innerHTML="谢谢">请点击该文本</h1>
  2. getElementById("").onclick = function(){
     displayDate();
     };
  3. getElementById("").addEventListener("click",function(){
     
     });
- window.screen
  1. window.screen对象再去爱编写时可以不使用window这个前缀。
  2. screen.availWidth;可用屏幕宽度
  3. screen.availHeight;可用屏幕高度
- window.location（window可以省略）
  1. location.hostname 返回web主机的域名
  2. location.pathname 返回当前页面的路径和文件名
  3. location.protocol 返回所使用的web协议（http://或https://）
  4. location.href 返回（当前页的）整个URL
- window.history
  1. window.history 对象在编写时候可以省略window前缀
  2. history.back() 和浏览器的后退按钮功能相同
  3. history.forward() 和浏览器中点击向前功能相同
  4. history.go() 






