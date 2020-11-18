# TortoiseGit 安装和使用教程
- 官网下载
- 安装步骤
- 创建版本库
- 工作流程
- 修改数据
- 添加数据
- 删除和恢复数据
- 推送到远程仓库
- 推送更新
- 解决冲突
- 搭建私有服务器
- 创建分支
- 常用编译器同步代码

## 官网下载
- [TortoiseGit安装包下载](tortoisegit.org/download/)
- [TortoiseGit汉化包下载](tortoisegit.org/download/)
- 避免360拦截，推荐使用谷歌浏览器下载

## 安装步骤
- 安装中勾选`OpenSSH,Git default SSH Client`
- 安装位置默认在C盘
- 安装完成后，右键会出现TortoiseGit图标
- 汉化包安装完成后
- 右键TortoiseGit图标，子菜单中点选Settings，面板中的Language下拉菜单选择中文即可

## 创建版本库
3种方式可创建版本库  
1. 通过TortoiseGit 右键-`Git在这里创建版本库`  
2. 通过Git 右键-`Git GUI Here`-`Create new repository`  
3. 通过Git 右键-`Git Bash Here`-`git init`  

版本库创建完成后，对应的文件夹里会出现`.git`隐藏文件夹，`.git`就是本地版本库，它对应的目录就是工作目录，一般要求工作目录是纯英文路径。包含`.git`的文件夹就是工作区，需要添加到仓库的内容，和`.git`保持在同一文件夹路径下面。  

## 工作流程
1. 将文件放置在工作区
2. 将文件添加至暂存区
3. 将文件提交到本地仓库
4. 将本地仓库推送至远程服务器(GitHub网站)  

如：在工作区新建一个txt文本，选中文本后，通过TortoiseGit 右键-`添加`  。

添加这一步骤只是把文本添加到暂存区。添加完成后，文本旁边会出现一个加号。

之后再通过TortoiseGit 右键-`Git 提交至->master`。在弹出面板中，填写日志信息，点击提交按钮。

提交完成后，文本旁边会出现绿色勾。

## 修改数据
- 这里要注意的是，每次对文本内容进行修改后，都可以重新提交。
- 还可以在工作区空白处，通过TortoiseGit 右键-`显示日志`，查看修改记录。
- 还可以选中两个版本，右键-`比较版本信息`
- 通过TortoiseGit 右键-`版本库浏览器`，查看本地仓库中的文件


## 添加数据
把一个项目工程文件加入到仓库中，步骤如下：

- 把项目文件复制到工作区里
- 选中文件夹后，通过TortoiseGit 右键-`添加`，也就是添加到暂存区
- 遇到不想要添加到仓库中的文件夹，选中它们，通过TortoiseGit 右键-`删除并添加到忽略列表`-`根据名称删除和忽略`
- 文件夹下面的其他内容需要一并忽略，就选择忽略类型为`递归忽略文件或目录`
- 内容还需保存在本地，只是不需要添加到本地仓库中，就选择忽略文件为`.gitignore放在文件/文件夹所在的目录`

忽略完成后，文件夹旁边会出现减号。

## 删除和恢复数据


## 推送到远程仓库
远程网络除了国外网站GitHub，还有国内的[码云](ttp://gitee.com)

2种推送方式：  
1. SSH推送，官网会有代码提示，这种方式需要用到秘钥（私钥和公钥）  
2. HTTPS推送，这种方式需要用到GitHub账号密码

SSH推送，秘钥生成步骤：
- 通过Git 右键-`Git Bash Here`
- 命令行输入`ssh -keygen -t rsa`
- 生成的秘钥，在当前电脑用户里，C盘-users-电脑用户名-`.ssh`文件

复制公钥，打开GitHub网站，点击用户头像-`settings`-`SSH and GPG keys`-`New SSH key`，把公钥粘贴在这里，建立GitHub网站和本地仓库的连接

**通过`Git`同步方式：**

- 在本地工作区，右键-`Git bash here`(origin远程仓库的别称)
- 输入`git remote add origin 路径`
- 把本地仓库推送给远程`git push -u origin master`
- 刷新GitHub网站，这样网站上的仓库和本地仓库内容就是一模一样的

**通过TortoiseGit同步方式：**
- 右键-`Git 同步`
- 设置面板中-网络-SSH客户端-C:\Program Files\Git\usr\bin\ssh.exe
- 设置面板中-Git-远端-输入URL(GitHub上复制的SSH码)-Putty密输入私钥位置-添加保存


HTTPS推送，不需要秘钥，需要用户名和密码

## 推送更新
克隆和下载，2种方式HTTPS或者SSH

SSH方式：
右键-`Git Bash Here`,输入`git clone 路径`

HTTPS方式：
右键-`Git克隆`

更新的记录，可以推送push到远程；远程更新了，也可以通过拉取pull，将远程更新拉取到本地

## 解决冲突
当本地和远程都进行了修改，出现冲突时，只能从远程拉取文件到本地，然后手动修改不同的地方。
右键-tortoisegit-`解决冲突`，然后提交到本地仓库，然后在推送到远程

## 搭建私有服务器

## 创建分支
- 切换/检出
- 创建分支
- 将分支合并，还可以删除分支

## 常用编译器同步代码
- 在jupyter notebook ,anocondas ,pycharm中怎么设置git代码同步
- 从git项目里怎么打开代码

