# Ajax_Simple_Demo
Ajax基础 来自网络   
## 简介  
AJAX 是一种在无需重新加载整个网页的情况下，能够更新部分网页的技术。   
浏览器通过触发事件，创建XMLHttpRequest对象，向服务器发送HttpRequest请求；服务器接收到请求之后,处理HttpRequest请求,返回结果数据给浏览器。  
请求访问的文件需要同源，而同源就是指URL中protocol协议、host域名、port端口这三个部分相同。  
www.baidu.com  ajax访问 http://www.baidu2.com 域名不同    
                        https://www.baidu.com 协议不同  
                        http://www.baidu.com:8080 端口不同  
## 示例代码

```
 function loadXMLDoc(url)
    {
        var xmlhttp;
        if (window.XMLHttpRequest)
        {// code for IE7+, Firefox, Chrome, Opera, Safari
            xmlhttp=new XMLHttpRequest();
        }
        else
        {// code for IE6, IE5
            xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
        }
        xmlhttp.onreadystatechange=function()
        {
            if (xmlhttp.readyState==4 && xmlhttp.status==200)
            {
                //解析传回来的数据
                document.getElementById('A1').innerHTML=xmlhttp.status;
                document.getElementById('A2').innerHTML=xmlhttp.statusText;
                document.getElementById('A3').innerHTML=xmlhttp.responseText;
            }
        }
        xmlhttp.open("GET",url,true);
        xmlhttp.send();
    }  
```  
## dom 

XML DOM 属性

一些典型的 DOM 属性：

    x.nodeName - x 的名称
    x.nodeValue - x 的值
    x.parentNode - x 的父节点
    x.childNodes - x 的子节点
    x.attributes - x 的属性节点

注释：在上面的列表中，x 是一个节点对象。    

XML DOM 方法

    x.getElementsByTagName(name) - 获取带有指定标签名称的所有元素
    x.appendChild(node) - 向 x 插入子节点
    x.removeChild(node) - 从 x 删除子节点

注释：在上面的列表中，x 是一个节点对象。





    
      

