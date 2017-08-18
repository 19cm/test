# 项目期第三天  git 

标签（空格分隔）： 项目

---
一. 思路
1 组长现在本地初始化一个laravel项目
github上创建一个仓库 blog
将项目推到远程的仓库上，远程仓库里就有了一个初始化的项目

2 组员从github的这个仓库中clone项目到本地

3 每个人开发自己的模块，创建自己的分支，将代码传到自己的分支上

4 组长先将组员对应分支的代码下载后自己电脑上，然后解决冲突，合并代码，合并分支后推送到远程的master分支上

5 组员在从mster分支上下载合并后的项目

6 如果再涉及到修改代码，从第2步重复操作

二. 团队使用github协作的步骤

1. 
```
提前准备工作
（1） 本地生成公私钥

告诉git 你是谁
git config --global user.name "github的用户名"
git config --global user.name gitfenger
git config --global user.email "github的账号"
git config --global user.email 414582343@qq.com


//本地端
//初始化git仓库
git init 
//复制一个laravel项目
composer create-project --prefer-dist laravel/laravel blog "5.2.*"
//添加到暂存区
git add .
//添加到版本库
git commit -m "项目初始化"
//github端
//申请github账号
//通过申请的账号，创建远程仓库 blog

//建立远程仓库和本地仓库的关联
git remote add origin git@github.com:gitfenger/blog.git
//将本地仓库推送到远程仓库
git push -u origin master

```

2
```
先设置自己git 的用户名 和 账号，尽量从组长那里拷贝一份公私钥，放到自己家目录的.ssh目录下

//组员从github的这个仓库中clone项目到本地
git clone git@github.com:gitfenger/blog.git
```
3 
```
//创建并切换分支
git checkout -b '分支名'
编辑你的模块
//推送到远程的对应分支
git push origin 你的分支名

```
4组长先将组员对应分支的代码下载后自己电脑上，然后解决冲突，合并代码，合并分支后推送到远程的master分支上
```
// 查看服务器有哪些新的分支更新
git fetch 
// 将组员刚提交的分支合并到本地项目
git merge origin/对应的要合并的分支的名称如zhangsan
// 推送到远程仓库
git push origin master

```

5组员在从mster分支上下载合并后的项目
```
直接从服务器的master分支拉取项目
git pull origin
````

