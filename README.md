# newLook
<h2>多房间聊天室</h2>
<ul>
	<h4>运行方式</h4>
	<li>基于node环境 如果没有包可自行npm install 安装依赖</li>
	<li>node 运行app.js服务访问端口号3000需要注意端口号的冲突</li>
	<li>默认访问public下面的index.html点击房间进入聊天室</li>
</ul>
<ul>
    <h4>基本技术</h4>
	<li>基于node环境搭建的express服务器</li>
	<li>通过express.Router路由传参方式判断房间号可以创建多房间</li>
	<li>通过jion加入房间 leave离开房间 通过socket.io自定义事件来传递消息</li>
	<li>利用hbs模板来渲染页面提高了代码的重用性 node可以下载hbs模块包通过require引用 set设置</li>
	<li>利用render方法返回给前端页面渲染数据</li>
</ul>
<ul>
    <h4>注意事项</h4>
	<li>node中的express中间件的版本区别	
	    <br>
	3和4的托管静态文件app.use(express.static('public'))新版本内置了static不用再reqiure引入否则报错</li>
	<li>
		路由传值来判断房间号(roomID)
		socketIO.to(roomID).emit()来指定发送的房间
	</li>
	<li>
		利用全局变量来存储用户名
	</li>
	<li>使用socket.io自定义事件来传递消息</li>
</ul>
