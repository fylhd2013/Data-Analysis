# Git Tutorial
- Git 初始化


## Git 初始化
基本信息设置
1. 设置用户名
	`git config --global user.name '用户名'`
2. 设置用户名邮箱
	`git config --global user.name '用户名邮箱'`

这个用户名和邮箱设置的用途是，在GitHub仓库主页显示是谁提交了该文件

## 初始化一个新的Git仓库
1. 创建文件夹
可以同右键创建文件夹，也可以通过命令行`mkdir 文件夹名`创建文件夹
2. 在文件内初始化Git(创建Git仓库)
	- 通过命令行`cd 刚创建的文件夹`进入刚创建的文件夹里面  
	- `git init`创建了`.git`文件

## 创建文件
- `touch 文件名.php`
- `git add 文件名.php`
- `git commit -m '添加提交描述'`
- `git status`

## 修改文件
- `vi 文件名.php 1.修改文件`
- `git status`
- `git add 文件名.php `2.添加到暂存区
- `git commit -m '添加提交描述'` 3.提交到仓库
- `git status`

## 删除文件
- `rm -fr 文件名.php`
- `git rm 文件名.php`
- `git commit -m '添加提交描述'`
- `git status`


## 将本地仓库同步到远程仓库
1. 克隆（目的是将远程仓库GitHub上对应的项目，复制到本地）
	- `git clone 仓库地址`仓库地址在GitHub网页上点击clone-clone with HTTPS
2. 创建文件
3. 添加到暂存区
4. `git push`推送到远程仓库

**设置上传权限**  
1. `vi .git/config`  
2. 将  
    `[remote "origin"]`
   ` url = https://github.com/用户名/仓库名.git`  
修改为：  
   ` [remote "origin"]`
    `url = https://用户名：密码@github.com/用户名/仓库名.git`



`git config --list` 可以查看已经初始化的信息，一般初始化一次往后都不用初始化了







## 常用Linus命令
- `pwd` 显示当前位置
- `touch 文件名.php` 创建文件
- `rm -rf 文件名.php` 删除文件
- `is`


## 搭建个人站点
访问 `https://用户名.github.io`
搭建步骤  
1. 创建个人站点  
	- 新建仓库（注：仓库名必须是`用户名.github.io`
2. 在仓库下新建`index.html`的文件即可

- GitHub pages 仅支持静态网页
- 仓库里只能是.html文件

## Project Pages 项目站点

访问 `https://用户名.github.io/仓库名`
搭建步骤  
1. 进入项目主页，点击settings
2. 在settings页面，点击`Launch automatic page generator`来自动生成主题页面
3. 新建站点基础信息设置
4. 选择主题
5. 生成网页
