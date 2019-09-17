# JavaScript

### Dom
	Js
	创建新节点
		creatElement()
		creatTextNode()
	
	操作节点
		appendChild()
		removeChild()
		replaceChild()
		insertBefore()
	查找
		getElementsByTagName()
		getElementsByClassName()
		getElementsByName()
		getElementById()
		querySeletor()
		
		eg:
		<ul class="test-ul">
		    <li>111</li>
		    <li>112</li>
		    <li>113</li>
		    <li>114</li>
		    <li>115</li>
		</ul>
		
		var lis = document.querySelector('.test-ul li')
		console.log(lis) // <li>111</li>
		var lis2 = document.getElementsByClassName('test-ul')[0].children
		console.log(lis2) // li li li li li
		var lis3 = document.getElementsByTagName('li')
		console.log(lis3) // li li li li li
		
	jQuery:
		append
		text
		html
		empty
		remove
		
		find('')
		children('')
		parentsUntil('')
		eq()
		siblings('')

### Function
	1. 函数声明 Function Declaration
	function func1 () {}
	2. 函数表达式 Function Expression
	var func2 = function () {}
	3. 构造函数
	new Function('a', 'b', 'return a + b');


### Ajax
	var xhr = new XHRHttpRquest();
	xhr.open('get',url,true);
	xhr.send();
	xhr.onreadystatechange = function(){
		if(xhr.readyState === 4 && xhr.status == 200){
			// do sth
		}
	}

### Promise
	var pro = new Promise((resolve,reject)=>{
			if(true){
				resolve(data)
			}else{
				reject(msg)
			}
		})
	pro.then((data)=>{
	
	}).catch((msg)=>{
		
	})

### Array
	直接修改arr
	push
	pop
	shift // 把数组的第一个元素从其中删除
	unshit // 向数组的开头添加一个或更多元素
	reverse
	sort arr.sort((a, b) => { return a - b })
	splice(index,count,new1,new2) // 替换原数组项目从index开始count个位置	
	
	新数组
	concat // 连接数组
	join // 数组变为字符串
	slice(start,end) 
	set 去重 Array.from(new Set(arr))
	
	arr.forEach( ()=>{} ) // 返回字符串，数组元素
	arr.map( ()=>{ return } ) // 加工原数组
	filter(function(item){ return type item == 'number'}) // 返回过滤后的数组,满足条件的留下

### JSON
	JSON.parse() 解析一个JSON字符串，构造由字符串描述的JavaScript值或对象
	JSON.stringify()

### 模块化
	commonJs
		服务器端模块规范，一个文件是一个模块，例如Node.js
		同步加载，程序在所有模块都加载完毕后才执行
	amd
	cmd

### jquery
	cdn https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js
	
	$(document).ready(function)
		* 当 DOM（文档对象模型） 已经加载，并且页面（包括图像）已经完全呈现时，会发生 ready 事件
		* onload 事件会在页面或图像加载完成后立即发生