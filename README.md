#  window.open不被拦截的解决方法

### 实现代码：

```
$obj.click(function(){
 var newTab=window.open('about:blank');
 $.ajax({
  success:function(data){
   if(data){
    //window.open('http://www.111cn.net');
    newTab.location.href="http://www.111cn.net";
   }
  }
 })
})
```
### 其他方法:

```
<script type="text/javascript">
<!-- 
$( 
function()
{
//方法一
window.showModalDialog("http://www.111cn.net/");
window.showModalDialog("http://www.111cn.net/");
 

//方法二
var aa=window.open();
setTimeout(function(){
aa.location="http://www.111cn.net";
}, 100);
 

var b=window.open();
setTimeout(function(){
b.location="http://www.111cn.net";
}, 200);
 

var c=window.open();
setTimeout(function(){
c.location="http://www.111cn.net";
}, 300);
 

var d=window.open();
setTimeout(function(){
d.location="http://www.111cn.net";
}, 400);
 

var ee=window.open();
setTimeout(function(){
ee.location="http://www.111cn.net";
}, 500);
 

var f=window.open();
setTimeout(function(){
f.location="http://www.111cn.net";
}, 600);
 

var g=window.open();
setTimeout(function(){
g.location="http://www.111cn.net";
}, 700);
 

var h=window.open();
setTimeout(function(){
h.location="http://www.111cn.net";
}, 800);
 

var i=window.open();
setTimeout(function(){
i.location="http://www.111cn.net";
}, 900);
 

var j=window.open();
setTimeout(function(){
j.location="http://www.111cn.net";
}, 1000);
 

//方法三
var a = $("<a href='http://www.111cn.net' target='_blank'>Apple</a>").get(0);
var e = document.createEvent('MouseEvents');
e.initEvent( 'click', true, true );
a.dispatchEvent(e);
 

var a = $("<a href='http://www.111cn.net' target='_blank'>Apple</a>").get(0);
var e = document.createEvent('MouseEvents');
e.initEvent( 'click', true, true );
a.dispatchEvent(e);
}
 
);
//-->
</script>
```
