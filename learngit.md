# Git
## 安装Git
### 配置
安装完成后，在命令行输入：
```
$ git config --global user.name "Your Name"
$ git config --global user.email"email@example.com"
```
## 创建版本库
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
## 时光穿梭机
查看工作区状态  
`$git status`  
查看工作区没有提交到stage的内容  
`$git diff [-- 文件名]`  
查看工作区没有正式提交的内容  
`$git diff head [-- 文件名]`  
### 版本回退

git remote add origin https://github.com/LiXiaohui1900/learngit.git
git push -u origin master