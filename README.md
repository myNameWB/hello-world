# hello-world
我的第一个GitHub存储库
这是一个简单的git上传nodejs代码到新浪云上的介绍
          
          Git上传代码到新浪云
          
1、首先下载git软件https://git-scm.com/downloads


2、打开git Bash使用cd D:\到d盘中，再使用命令git clone https://github.com/sinacloud/nodejs-getting-started.git下载下来文件，到D盘中找到nodejs-getting-started.git，主要拿到package.json文件，复制到自己文件根目录下。

3、在git上登录本地用户名：
	git config --global user.name "用户名"
	git config --global user.email "邮箱"
	//用户名和邮箱，是自己创建的本地仓库用户名和邮箱

4、再重新打开git，cd到你的nodejs文件目录下

5、把本地的文件中的主文件，不如说启动文件，名称改为：index.js，
并把监听的端口号改为：5050端口。
接着，把pool里面的连接池都改为：
var connection = mysql.createConnection({
    host     : process.env.MYSQL_HOST,
    port     : process.env.MYSQL_PORT,
    user     : process.env.ACCESSKEY,
    password : process.env.SECRETKEY,
    database : 'app_' + process.env.APPNAME
});
6、git init创建本地仓库
7、git add . //添加到暂存区里面去

8、git remote add sinacloud https://git.sinacloud.com/helloworld  //helloWord是你自己新浪云的存储空间，记得要改

9、在当前目录下，执行npm start执行，如果没有出错就可以继续执行，否者找出错误（如果没有出错，就直接Ctrl+c退出，继续执行下面的操作）

10、git add .   上传所有文件
11、git commit -m "Init my first app"    //“Init my first app”是注释用的

12、git push sinacloud master 
// 把本地仓库的代码推送到新浪云仓库，此步需要输入新浪云的账号和安全密码

13、如果执行还是执行失败，就看下你的nodejs文件夹下.git文件中的config中把https://git.sinacloud.com/....    //改成和你新浪云中的一样就可以了
