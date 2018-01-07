#git学习笔记


## 基本概念

- 使用GitHub的意义： 借助github托管项目代码

- Repsository 仓库：用于存放项目代码，对应一个项目

- Star 收藏：便于反复查看

- Fork 克隆：完全复制别人的仓库，并独立存在。

- Pull request发起请求：他人在fork的项目中作出更改，使用Pull 

- request后征求原作者的同意，更新到原项目之中。

- Watch 关注：关注项目更新，可接收到通知。

- Issue 事务卡片：发现bug时提出问题，讨论时使用。

- Github主页： 左侧主要为用户和关注用户动态，右侧显示所有Git库

- 仓库主页：显示项目代码，版本，收藏等项目信息

- 个人主页 ：个人信息

	### 使用issues
	Issues：发现BUG 或使开源项目出现问题时向开发者反馈使用
	关闭是双方都有的 	

##使用Git##

### Git的三个工作区：
* 工作区 working directory：修改、选择等操作

* 暂存区： 暂时存储

* Git Repository： Git 仓库

工作流及相应命令符：

	Git status:显示文件的状态

	Git add hello.php:将hello.php从工作区提交到暂存区

之后应再使用一次Git status确认文件状态

	Git commit –m”提交描述”

## Git的基本操作
显示是谁提交了文件

设置用户名

	Git config --global user.name ‘用户名’

设置用户名邮箱

	Git config –global user.email ‘用户名邮箱’

查看设置

	Git config --list

### 初始化新的Git仓库 
创建新的文件夹   

	Mkdir 仓库名 
在文件内初始化git  
	
	Pwd  显示当前路径
	Cd <Folder>   进入
	Git init    建立git
	这时便生成名为.git的隐藏文件，设置该文件夹存储仓库信息

### 向仓库提交文件
	Touch <file>   创建一个文件
	Add <file> 提交一个文件至暂存区
	Git commit –m”提交描述”
  
### 修改仓库中的文件
	Vi <file> 进入修改文件
	Cat <file> 现实文件内容
	之后按提交文件的流程

### 删除仓库中的文件
	Rm <file> 删除文件
	Rm –rf <file>  删除文件
	Git rm <file> 从git中删除文件
	Git commit –m ‘提交描述’

### git管理远程仓库
即是Git克隆操作  
作用：备份，实现共享

将远程仓库 github对应仓库下载到本地


	Git clone <仓库地址>


在提交到Git Repository后使用git push将本地仓库提交到远程

###解决git push 错误

为私有项目，没有权限，输入用户名密码，或远程地址采用这种类型：

	Vi .git/config
	 
	[remote “origin”]
		url = https://github.com/用户名/仓库名/.git
	改为 
		url = https://用户名:密码@github.com/用户名/仓库名/.git


