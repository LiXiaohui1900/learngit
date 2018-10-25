# Git
## 安装Git
### 配置
安装完成后，在命令行输入：
```
$ git config --global user.name "Your Name"
$ git config --global user.email"email@example.com"
```
## 创建版本库及提交
初始化版本库  
`$git init`  
添加文件  
`$git add 文件名`  
删除文件  
`$git rm 文件名`  
删除文件夹  
`$git rm -fr 文件夹名`  
提交修改  
`$git commit -m "注释"`  
## 版本控制
### 查看状态
查看工作区状态  
`$git status`  
查看工作区没有提交到stage的内容（按`q`退出）  
`$git diff [-- 文件名]`  
查看工作区没有正式提交的内容  
`$git diff head [-- 文件名]`  
head表示当前版本，表示之前版本的方式是：`head^``head^^``head~5`等等  
### 版本回退
退回到之前版本  
`$git reset --hard commit_id`  
查看提交历史  
`$git log [--pretty=oneline]`  
查看历史命令，可以查看未来版本  
`$git reflog`  
### 撤销修改
丢弃工作区修改，回到stage中的状态（注意:"--"很重要，如果没有"--"就是切换到另一分支的命令）  
`$git checkout -- 文件名`  
把stage中的内容退回到HEAD（此时工作区内容不变）  
`$git reset head 文件名`  
## 远程仓库
1. 创建SSH Key：  
`$ssh-keygen -t rsa -C "email@example.com"`  
如果一切顺利的话，可以在用户主目录里找到`.ssh`目录，里面有`id_rsa`和`id_rsa.pub`两个文件，这两个就是`SSH Key`的秘钥对，`id_rsa`是私钥，不能泄露出去，`id_rsa.pub`是公钥，可以放心地告诉任何人。  
2. 登陆GitHub，右上角Settings --> SSH and GPG keys --> New SSH key  


git remote add origin https://github.com/LiXiaohui1900/库名.git
git push -u origin master