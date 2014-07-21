什么是git
======
    Git 是用于Linux 内核开发的版本控制工具。与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持，使源代码的发布和交流极其方便。 Git 的速度很快，这对于诸如 Linux kernel 这样的大项目来说自然很重要。 Git 最为出色的是它的合并跟踪（merge tracing）能力。

git常用命令
======

1、安装：
------
	$ sudo apt-get install git

	$ sudo apt-get install gitk#此为安装官方的图形界面，不需要的可以不安装

2、cd到需要管理的代码、文件所在的第一级目录
------
 
3、初始化：
------
	$ git init

4、添加当前目录所有内容：
------
	$ git add .

5、查看状态：
------
	$ git status

6、添加commit：
------
	$ git commit -am "first commit."

7、版本对比：
------
	$ git diff

8、查看历史记录：
------
	$ git log

9、分支操作
------
	查看分支：$ git branch
	创建分支：$ git branch 分支名称 （注意：请不要在服务端建立分支）
	切换分支：$ git checkout 分支名称
	删除分支：$ git branch -d 分支名称

10、加入服务器
------
	$ git remote add 用户名@计算机名或IP:~/某个目录

11、推送数据
------
	$ git push master master #本地master推送到远端master

	如果想快捷的使用git push就推送到默认远端分支master，可以做个一次性设置：
	$ git remote add origin <实际的ssl用户名>@<IP地址>:<Git在远端的path>
    做完以上设置，以后直接使用git push 就会自动推送到上述设置地址了，但如果要推送到其他分支，还是需要加参数的，这个设置只是相当于一个默认参数而已。

12、接收数据
------
	$ git pull origin master
	如果想直接使用git pull直接接收，同样需要提前做一个一次性设置（同样也是不能应用多分支pull情况）：
	$ git branch --set-upstream master origin/master

13、本地库设置个人姓名和邮件
------
	$ git config --global user.name "你的姓名，最好由没有符合和空格的英文字母组成"
	$ git config --global user.email <邮件名>@<邮箱服务商后缀>
	如果不设置个人信息，提交的信息将不会有更改者信息，这样会加大项目管理的难度。

14、启动图形界面
------
	$ gitk