
ieBetter.js
================
It's created for IE6-IE8.


Why need this?
-----------------
Modern browsers are so powerfull. For some small project, this is no any reason to include a large JavaScript library. For example, jQuery, Kissy and so on.

So, what we need is just a file of JavaScript witch is created only for IE6-IE8, and make IE6-IE8 like a modern browser(Chrome, IE9+, ...).

How to use?
----------------
Simplely, include 'ieBetter.js', then just use APIs as in modern browser. For example, you can use <code>document.querySelector</code> to select the DOM element, and so on. The APIs that you can use see below.

<pre>document.querySelector("#id");</pre>

Because of that only IE6-IE8 need ieBetter.js. So we have to do some special deal. For Example, IE conditional comments. Like this:
<pre>&lt;!--[if lte IE 8]>
&lt;script src="ieBetter.js">&lt;/script>
&lt;![endif]--></pre>

However, IE10+ begin to ignore conditional comments. So, for this browser, if the page is in a IE6-IE8 documentMode, <code>ieBetter.js</code> will be ignore. So, maybe you can try this method:
<pre>if (!document.addEventListener) {
    // IE6~IE8
    document.write('&lt;script src="ieBetter.js">&lt;\/script>');	
}</pre>

Good luck for you!

APIs and Demos
------------------
So far, the APIs that has supported are: <br><br>
<strong>• 选择器相关API</strong><br>
*.querySelector<br>
*.querySelectorAll<br>
*.getElementsByClassName<br><br>
<strong>• 事件相关API</strong><br>
*.addEventListener<br>
*.removeEventListener<br>
*.dispatchEvent<br>
document.createEvent<br>
init[|Mouse|UI]Event<br>
input<br>
window.onhashchange<br><br>
<strong>• DOM特性相关API</strong><br>
window.getComputedStyle<br><br>
<strong>• ES5 JSON扩展</strong><br>
JSON.parse<br>
JSON.stringify<br><br>
<strong>• ES5 Object扩展</strong><br>
Object.create<br>
Object.keys<br><br>
<strong>• Date对象</strong><br>
Date.now<br><br>
<strong>• ES5 Function扩展</strong><br>
Function.bind<br><br>
<strong>• ES5 String扩展</strong><br>
String.trim<br><br>
<strong>• ES5 数组方法扩展</strong><br>
Array.isArray<br>
Array.forEach<br>
Array.map<br>
Array.filter<br>
Array.some<br>
Array.every<br>
Array.indexOf<br>
Array.lastIndexOf<br>
Array.reduce<br>
Array.reduceRight

You can visit API document to get more infomation: [http://rawgithub.com/zhangxinxu/ieBetter.js/master/index.html](http://rawgithub.com/zhangxinxu/ieBetter.js/master/index.html)

Still, you can [visit here](http://www.zhangxinxu.com/wordpress/?p=3835) to some other information.


License
-------------------
[The MIT License](https://github.com/zhangxinxu/ieBetter.js/blob/master/LICENSE.md)

Donate
------------------
<a target="_blank" href="https://me.alipay.com/zhangxinxu" title="小小赞助大大帮助"><img src="http://www.zhangxinxu.com/wordpress/wp-content/themes/default/images/pay_encourage.png" width="159" height="37" alt="支付鼓励" align="absmiddle"></a>




