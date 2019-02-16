# git 命令行

## 1. 本地操作
``` 
git init 本地初始化一个仓储
git status 查看有哪些文件添加、或者没有添加到仓储中
git add .  git add --all 添加所有文件(每次重新提交前必须先添加)，如果有忽略文件，需要在本地根目录下创建一个.gitignore文件（忽略文件直接写目录名，文件名一行一个）
git commit -m 'xxx' 每次提交的信息
git log 提交后查看提交日志，如果需要重新回到之前的版本 则需要取版本号的前7位
git reset --head 1df0573
git rm --cache 文件名  从跟踪中移除某个
git rm --cache -r 文件夹名
touch .gitignore 创建.gitignore 文件

```
## 2. 同步到github
``` 
# 远程添加源 
git remote add origin https://github.com/kurongdashi/angular.git 
# 查看是否已经添加了源
git remote 
# 将本地提交的文件同步到github -u是以流的方式提交 push推送 到 origin 的master分支
git push -u origin master  
# 获取github上的最新版本
git pull origin master  

```


注意：直接在github上修改文件后，下次提交前必须先从github上同步一份到本地，然后才能提交 git pull origin master

## 3.分支操作
``` 
# 查看当前所有的分支  注意：（版本升级就需要创建新的分支）
git branch 
# 在本地创建一个新的分支(必须在第一次提交到master分支后，才能创建新的分支)
git branch v2 
# 选择v2分支
git checkout v2 
# 将v2分支同步到github
git push -u origin v2 

```
## 4.克隆到本地
``` 
# 克隆一套代码到本地 .代表当前目录
git clone https://github.com/kurongdashi/angular.git .
```
## 5.演示站，搭建

1. 将项目提交到github的gh-pages 分支，可以在线预览，演示了  
>地址：https://kurongdashi.github.io/show/

说明：
``` 
自己的ID.github.io/仓储名（或者仓储下/项目）
```
 
 
2. 将仓储名 命名为：自己的ID.github.io 则它的master分支也可以在线访问了
