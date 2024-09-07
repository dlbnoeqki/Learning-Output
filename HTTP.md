>http超文本传输协议是位于TCP/IP体系结构的应用层协议，它是WWW数据通信的基础。

访问一个网站时，需要通过一个统一资源定位符【URL】来定位服务器并获取资源。
> <协议>://<域名>:<端口>/<路径>


session
cookie
## http/1.1
http/1.1是目前使用最广泛的版本，一般没有特别注明版本都是指http/1.1。
### http连接建立过程

1. 通过DNS将域名转换为IP地址。
2. 通过三次握手建立TCP连接。
3. 发送http请求。
4. 目标服务器接收到http请求并处理。
5. 目标服务器往浏览器发回http响应。
6. 浏览器解析并渲染页面。
### http连接拆过过程



### http报文格式
http报文由三个部分组成，它们之间由CRLF【回车换行符】分隔开。
- 请求行
- 首部
- 实体



什么是http2

http2与http的区别

http2实践

### http性能优化

减少http请求
静态资源使用cdn
善用缓存
压缩文件

## https
>https是http协议的安全形式。使用https时，所有的http请求和响应数据在发送之前，都要进行加密，加密可以使用SSL或TLS。

### https的加密算法
对称加密
非对称加密
摘要算法
数字签名
数字证书
### https连接建立过程


## HTTP/2
>HTTP/2是HTTP/1.x的扩展，而非替代。所有HTTP的语义不变。


http服务器就是web服务器
web服务器中的资源不只是静态文件，也可以是一些程序

MIME类型是一种文本标记，表示一种主要的对象类型和一个特定的子类型，中间由一条斜杠来分隔。
text/html
text/plain
image/jpeg
image/gif

URI：web服务器资源的名字，它是一个唯一标识
http://www.joes-hardware.com/specials/saw-blade.gif
URI指示HTTP协议去访问


