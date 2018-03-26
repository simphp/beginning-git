# Beginning Git

## 1.Git简介
Git: 分布式版本管理系统

## 2.安装Git

### Linux上安装Git
`sudo apt-get install git`

### MacOS上安装Git
* 通过`homebrew`安装
* 通过`Xcode`安装

### Windows上安装Git
Git官网下载安装程序

## 3.设置用户信息
### 全局设置
`$ git config --global user.name "Userame"`
`$ git config --global user.email "email@xxx.com"`
### 对某个仓库设置

## 4.本地仓库操作

### 初始化仓库
`$ git init`

### 把文件添加到暂存区
`$ git add <file>`

### 把文件提交到当前分支
`$ git commit -m "提交说明"`

### 查看当前状态
`$ git status`

### 比较文件差异
* 比较工作区与暂存区差异：`$ git diff <file>`
* 比较暂存区与最新本地版本库： `$ git diff --cached <file>`
* 比较工作区与最新本地版本库： `$ git diff HEAD -- <file>`
* 比较工作区与指定版本： `$ git diff <版本号> <file>`
* 比较暂存区与指定版本： `$ git diff --cached <版本号> <file>`
* 比较两个版本： `$ git diff <版本号> <版本号>`

### 查看提交日志
`$ git log`
参数：`--pretty=oneline`

### 版本回滚
* 回滚到上1个版本 `$ git reset --hard HEAD^`
* 回滚到上2个版本 `$ git reset --hard HEAD^^`
* 回滚到上n个版本 `$ git reset --hard HEAD~n`
* 跳转到指定版本 `$ git reset --hard <版本号>`

### 查看所有操作记录
`$ git reflog`

### 撤销修改
撤销工作区的修改： `$ git checkout -- <file>`
撤销暂存区的修改： `$ git reset HEAD <file>`

### 删除文件
删除文件： `$ git rm <file>`
撤销删除： `$ git checkout -- <file>`