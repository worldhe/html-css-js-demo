CSS选择器

- 元素选择器（通过html标签名）
  通过元素选择器可以选择页面中指定的所有元素。
  p {
  }
  div {
  }
  span {
  }
  ......
- id选择器
  通过元素的id属性值选中唯一的一个元素。
  #id属性值。
- class选择器
  class属性和id属性类似，只不过class属性可以重复拥有相同的class属性值，我们说他们是一组元素。
  可以同时为一个元素设置多个class属性值，多个属性值之间使用空格隔开。即<p class="first second"></p>
  .class属性值。
- 选择器分组
  通过选择器分组可以同时选中多个选择器对应的元素，即满足选择器1的，并且满足选择器2的，并且满足选择器n的，全部元素选中。
  选择器1，选择器2，选择器n {
  }
- 通配选择器
  可以选择页面中所有的元素。
      * {
          
      }
  
- 复合选择器（交集选择器）
  可以选中同时满足多个选择器的元素
  选择器1选择器2选择器n {
  }
      <p class="p1">
      <span class="p1">
      //要求：为拥有class等于p1，并且是span元素的背景设置红色。
      span.p1 {
          background-color:red;
      }
  
- 元素之间的关系
  父元素：直接包含子元素的元素。
  子元素：直接被父元素包含的元素。
  祖先元素：直接或间接包含后代的元素，父元素也是祖先元素。
  后代元素：直接或间接被祖先元素包含的元素，子元素也是后代元素。
  兄弟元素：拥有相同父元素的元素。
- 后代元素选择器
  div span {
  }
      <div>
      	<span></span>
      </div>
  
- 子元素选择器
  选中指定父元素的指定子元素
  父元素 > 子元素
- 伪类选择器
  伪类：专门用来表示元素的一种特殊的状态。
  例如：访问过的超链接，普通的超链接，获取焦点的文本框。
  当我们需要为处在这些特殊状态的元素设置，就可以使用伪类。
  a:link	正常链接
  a:visited	访问过的链接（只能定义字体颜色）
  a:hover	鼠标划过的链接
  a:active	正在点击的链接
- 使用伪元素表示元素中的一些特殊的位置
  eg：为p中第一个字符来设置一个特殊的样式
      p:first-latter {
          color:red;
          font-size:20px;
      }
  eg:为p中第一行设置一个背景颜色
      p:first-line {
          background-color:red;
      }
  :before表示元素最前面的部分
  一般before都需要结合content这个样式一起使用
  通过content可以想before活after的位置添加一些内容
      p:before {
          content:"我会出现在整个段落的最前面";
          color: red;
      }
      p:after {
          content:"我会出现在整个段落的最后面";
          color: orange;
      }
  
- 属性选择器
  可以根基元素中的属性或属性值来选取指定元素。
  [属性名]选取含有指定属性的元素。
  [属性名="属性值"]选取含有指定属性值的元素。
  [属性名^="属性值"]选取属性值以指定内容开头的元素。
  [属性名$="属性值"]选取属性值以指定内容结尾的元素。
  [属性名*="属性值"]选取属性值以包含指定内容的元素。
      <p title="hello">我是一个段落</p>
      <p>我是一个段落</p>
      <p>我是一个段落</p>
      <p>我是一个段落</p>
      <p>我是一个段落</p>
      <p title="abc">我是一个段落</p>
      
      p[title] {
          background-color:red;
      }
      
      p[title="abc"] {
          background-color:blue;
      }
  
- 
  
  

CSS：visibility

- 可以用来设置元素的隐藏和显示状态
  可选值：
  visiable：默认值，元素默认会在页面显示。
  hidden：元素会隐藏不显示，但是元素还回在页面中继续占有位置。

CSS：display

- 将一个行内元素变成块元素
- 通过display样式可以修改元素的类型
  可选值：
  inline：可以将一个元素作为行内元素显示
  block：可以将一个元素设置为块元素
  inline-block：讲一个元素转换为行内块元素（可以使以一个元素即有行内元素的特点，又有块元素的特点，可以设置宽高，又不会站一行）
  none：此元素不会显示，并且元素不会在页面中继续占有位置。
  

CSS：overflow

- 子元素默认是存在父元素内容区中。
- 理论上讲子元素的最大可以等于父元素内容区的大小。
- 如果子元素的大小超过了父元素的内容区，则超过的大小会在父元素以外的位置显示。
- 超出父元素的内容我们称为溢出内容。
- 父元素默认是将溢出的内容，在父元素外边显示。
- 通过overflow可以设置父元素如何处理溢出内容
  可选值：
  		visiable：默认（不会对溢出内容处理，元素会在父元素以外显示）
  		hidden：内容被修建，其余内容不可见（溢出的内容会被修建，不会显示）
  		scroll：会为父元素添加滚动条，通过拖动滚动条来查看完整内容，改属性不论内容是否溢出，都会添加水平和垂直方向的滚动条。
  		auto：会根据需求自动添加滚动条
  				需要水平就添加水平，需要竖直就添加竖直。

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






