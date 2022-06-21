# JSMultipartParse

* 浏览器环境解析 gzip
* 浏览器解析 multipart 格式的文件


## gzip 解压 
最先使用的是 pako.inflate.js，测试基本没有问题。但是使用了一段时间，发现一些问题，文件解压没有报错(项目中的 gzip 文件)，但是后续处理会有问题，更换最新的版本 pako_inflate_2.0.4.js 解压会报错。
但是这个文件用 java 解析都没有问题，使用 gunzip.min.js 解压结果也是对的。

## multipart 解析

浏览器环境和 node.js 环境还是不同的，有些东西浏览器没有，但是浏览器有ArrayBuffer、Uint8Array,那问题就不大，照着 node.js 环境的代码将浏览器不支持的东西替换掉就可以。
