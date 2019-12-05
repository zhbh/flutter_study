###day2学习

- 内容
	1. 路由与路由表
		1. 路由对象实现页面生成
			1. 概念理解，路由指的是一个页面显示，而不是路径分配；
			2. PageRoute类生成路由页面，就是一个模态页面，而MaterialPageRouter类是继承PageRoute类；
			3. MaterialPageRoute是一种组件风格主题（andriod）的页面。
		2. 路由表生成页面
			总页面MaterialApp的routes属性注册路径：
			`routes: {
				'new_page': (context) => NewPage([参数])
			}`
	2. 路由管理
		1. 页面跳转，就需要路由管理Navigator类；
		2. Navigator有相应的方法，例如pop方法（页面退出），push方法（页面弹出）等等；
		3. 对路由表用pushName('new_page')方法实现页面弹出，其中参数是routes中注册的名字。
	3. 路由返回值
		1. 一个页面到另个新的页面，可以通过类的实例创建时候，给成员赋值；
		2. 页面返回之前的页面，可以Navigator.pop方法第二个参赛返回，让push方法返回值异步接收返回值。
