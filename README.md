因为用的是免费空间，希望大家尽量不要折腾大流量的东东，比如用于下载和视频。

goproxy-php模式简解
goproxy下载
https://github.com/goproxy0/goproxy/releases

git部署到heroku
1、注册一个Heroku账号： https://signup.heroku.com/signup/dc

2、访问 https://github.com/yeahwu/goproxy/tree/server.php-go

3、点击 Readme.md 页面下面紫色 deploy to heroku
https://dashboard.heroku.com/new-app?template=https://github.com/yeahwu/goproxy/tree/server.php-go
https://dashboard.heroku.com/new-app?template=https://github.com/zhaodiao/goproxy/tree/server.php-go

4、输入你想要的名称，服务器随意 US 或 EU

goproxy 的使用方法
修改 goproxy 目录下的 php.json 文件中的 Url，可以填写多个app

{
	"Servers": [
		{
			"Url": "https://appname1.herokuapp.com/",  
			"Password": "123456",
			"SSLVerify": true,
			"Host": "",
		},
		{
			"Url": "https://appname2.herokuapp.com/", 
			"Password": "123456",
			"SSLVerify": true,
			"Host": "",
		}
	],
修改 httpproxy.json 文件

"Default": {
	"Enabled": false, //这个是默认的gae模式，关闭或打开都可以，俺是关闭的

"PHP": {
	"Enabled": true,  //这个必须改成 true 打开
修改完上面两处就可以运行 goproxy，windows 点击 goproxy-gui.exe 运行，Linux 直接 cd 到文件夹 ./goproxy ，

goproxy php 默认的代理主机端口是:

http 127.0.0.1 8088 //建议配合 Proxy SwitchyOmega 使用

安装证书同XX-Net，这里就不多讲了。
