ShootPlane - 仿微信打飞机游戏的java实现
===========================================

## 效果图
![首页](shootplane_1.png)
![运行](shootplane_2.png)

## 文件夹结构
	images      本项目所用到的图片文件，从微信的apk里面解压出来的，稍微处理了一下 
	sound       本项目所用到的声音文件，从微信的apk里面解压出来的，原来是mp3格式，转成了java可以播放的wav格式 
	src         本项目的源代码
	publish     项目发布时的一些有用的启动脚本
	help.html   本项目的帮助文件
	score.dat   自动生成的用来保存序列化后的最高10个分数的文件

## 源码结构
	config      项目的配置类目录
	entity      项目的实体类目录
	factory     项目的武器，子弹，敌机的创建工厂类
	listener    项目的武器，子弹，敌机的位置改变监听接口
	ui          项目的图形界面类
	util        项目的工具类，文件操作，声音播放
	
## 编译（在Mac或Linux下，Windows类似）
	1. 进入目录ShootPlane/ShootPlane，该目录下有src等子目录
	   `cd ShootPlane/ShootPlane`
	2. 建立子目录bin，如果还没有的话
	   `mkdir bin`
	3. 编译src目录下的Java源文件，生成class文件于bin目录下
	   `find src -name '*.java' -exec javac -d bin/ {} +`
	4. 把bin目录下的内容打包成jar文件
	   `jar cvf ShootPlane.jar -C bin .`

## 运行程序
确保上面生成的ShootPlane.jar与images，sound，help.html，score.dat在同一目录下，然后在该目录下执行

`java -cp ShootPlane.jar com.beancore.Main`
