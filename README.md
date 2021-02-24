**GIT**  

https://www.liaoxuefeng.com/wiki/896043488029600
https://www.cnblogs.com/qdhxhz/p/9757390.html 

Git本地有四个工作区域:工作目录(Working Directory)、暂存区(Stage/Index)、资源库(Repository)、git仓库(Remote Directory)。文件在这四个区域之间的转换关系如下:
![](https://img2018.cnblogs.com/blog/1090617/201810/1090617-20181008211557402-232838726.png)

<font color=#FF7F27>Workspace</font> : 工作区,就是你平时存放项目代码的地方  
<font color=#FF7F27>Index / Stage</font>:暂存区,用于临时存放你的改动，事实上它只是一个文件，保存即将提交到文件列表信息  
<font color=#FF7F27>Repository</font>:仓库区（或版本库），就是安全存放数据的位置，这里面有你提交到所有版本的数据。其中HEAD指向最新放入仓库的版本  
<font color=#FF7F27>Remote</font>:远程仓库，托管代码的服务器，可以简单的认为是你项目组中的一台电脑用于远程数据交换

### 1.本地代码提交到远程服务

1) > 把代码变成 git 可以管理的仓库  
    `git init`
 
2) > 添加文件到暂存区  
    `git add .  //添加所有文件到暂存区 `
    <br>
    `git add test.txt  //添加单个文件 `
     
3) > 把文件提交到仓库   
    `git commmit -m 'decriptions' `
     
4) > 关联远程仓库<font color=red>(第一次使用需要添加)</font>   
   `git remote add origin http://127.0.0.1:8888/yepeng/ExScheduler.git `

5) > 获取远程库与本地同步<font color=red>(远程仓库不为空需要这一步)</font>   
    `git pull --rebase origin master`

6) > 把本地内容推送到远程库  
    `git push -u origin master`

    <font color=red>**提示:如果是从 GitLab clone下来的代码，则只要进行 2->3->5->6 这四个步骤**</font>


### 2.显示工作目录和暂存区的状态

*  `git status`

### 3.查看git 提交日志

* `git log`
* 退出提交日志，请按 `q` 键

### 4.撤回修改的代码

* > 撤回指定修改的文件  
    `git checkout 文件名`
* > 撤回所有修改的文件
    `git checkout . `

### 5.查看 git 用户信息

* > 显示当前的 Git配置  
`git config --list`

* > 查看用户名  
`git config user.name`

* > 查看用户邮箱  
`git config user.email`

* > 修改用户名和邮箱  
`git config --global user.name "jinlong"`  
`git config --global user.email "xxx@qq.com"`


### 6.分支 <font color=red>待完善</font>
* > 列出所有本地分支  
`git branch`

### 7.查看单个文件的内容

* `cat test.txt`

### 8.删除远程仓库文件，但是保留本地文件

    第一步：git rm --cached -r 文件名/或文件夹名
    第二步：git commit -m "remove file"
    第三步：git push

### 9.git tag

* > 查看标签
    `git tag`

* > 创建标签
   `git tag -a v1.0 -m 'my version 1.0'`


### 10.test
