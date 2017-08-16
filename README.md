# validateFileUpload.js插件介绍

validateFileUpload.js用于文件上传时进行格式、大小等规则校验，成功与否都执行回调函数，采用ES6语法，不依赖其他库，可单独运行。

### 使用说明

### html

``` html
<input type="file" id="file" />
<img src="http://www.zymseo.com/images/logo.jpg" alt="图片" id="img" />
<button id="btn">按钮</button>
```

### （1）script标签引入

``` javascript
<script type="text/javascript" src="./validateFileUpload-es6.js"></script>
<script type="text/javascript">
	validateFileUpload({
		fileType : ['jpg', 'jpeg', 'png', 'bmp'],
		maxSize : 2,
		inptEle : document.querySelector('#file'),
		showEle : document.querySelector('#img'),
		success : function (res) {
			console.log(res);
		},
		error : function (res) {
			console.log(res);
		}
	});
</script>
```
### （2）require方法异步引入：
``` javascript
require(['validateFileUpload'], function (validateFileUpload) {
	validateFileUpload({
		fileType : ['jpg', 'jpeg', 'png', 'bmp'],
		maxSize : 2,
		inptEle : document.querySelector('#file'),
		showEle : document.querySelector('#img'),
		success : function (res) {
			console.log(res);
		},
		error : function (res) {
			console.log(res);
		}
	});
});
```
### （3）ES6语法引入：
``` javascript
import validateFileUpload from './validateFileUpload-es6.js';
validateFileUpload({
		fileType : ['jpg', 'jpeg', 'png', 'bmp'],
		maxSize : 2,
		inptEle : document.querySelector('#file'),
		showEle : document.querySelector('#img'),
		success : function (res) {
			console.log(res);
		},
		error : function (res) {
			console.log(res);
		}
	});
```
### validateFileUpload.js可与[@文件上传插件](https://github.com/zymseo/iframeFileUpload)配合使用！
### 插件遵循Apache开源许可协议
- 博客：[@赵一鸣](http://www.zymseo.com)
- QQ：1047832475