# git设置用户名

git config user.name hongli

git config user.email hongli_stu@163.com(用作：唯一标识)

信息保存位置：.git/config

系统用户级别：--global   加参数  git config --global user.name hongli

信息保存位置：~/.gitconfig

# 基本操作

状态查看操作：git status

查看工作区状态

添加操作：git add[file name]  将工作区的“新建/修改”添加到暂存区

提交操作：git commit -m "commit message" [file name]

查看历史记录操作：

git log

git log --pretty=online

git log --online （只显示过去）

git reflog （显示全部）

前进后退：git reset --hard [局部索引值]

使用^  只能回退：git reset --hard HEAD^  一个^ 表示后退一个，n个表示后退n个

使用~ 只能后退：git reset --hard HEAD~n 表示后退n步

删除文件并找回：

前提：删除前，文件存在时的状态提交到了本地库

操作：git reset --hard[指针位置]

删除操作已经提交到本地库：指针位置指向历史记录

删除操作尚未提交到本地库：指针位置使用HEAD

比较文件差异：

git diff [文件名]

将工作区中的文件和暂存区进行比较

git diff [本地库中历史版本] [文件名]

将工作去中的文件和本地库的历史记录比较

不带文件名比较多个文件

# 分支管理

什么是分支：

在版本控制过程中，使用多条线同时推荐多个任务

分支的好处：

同时并行推进多个功能开发，推高开发效率

各个分支的开发过程中，如果某一个分支开发失败，不对对其他分支有任何影响

# 分支操作

创建分支：

git branch [分支名]

查看分支：

git branch -v

切换分支：

git checkout [分支名]

合并分支：

第一步：切换到接受修改的分支（被合并，增加新内容）上

git checkout [被合并的分支名]

第二步：执行merge命令

git merge [新内容的分支名]

解决冲突：

第一步：编辑文件，删除特殊符号

第二步：把文件修改到满意的程度，保存退出

第三步：git add [文件名]

第四步：git commit -m "日志信息"

注意：此时 commit一定不能带具体文件名

# git远程库

git remote -v 查看当前所有远程地址别名

git remote add [别名] [远程地址]

推送：

方式：git push [别名] [分支名]

克隆：

命令：

git clone [远程地址]

效果：

完整的把远程库下载到本地

创建origin远程地址名

初始化本地库 

拉取：

pull=fetch+merge

git fetch [远程库地址别名] [远程分支名]

git merge [远程库地址别名/远程分支名]

解决冲突：

要点：

如果不是基于Github远程库的罪行版所做的修改，不能推送，必须先拉取。

拉取下来后，如果进入冲突状态，则按照”分支冲突解决“操作即可

# SSH登录

创建ssh key

ssh-keygen -t rsa -C "1825123609@qq.com"

新建远程地址的别名：

git remote -v 查看当前所有远程地址别名

git remote add [别名] [ssh远程地址]

# git工作流

 gitlab安装：查下是干嘛的->(视频链接)[https://www.bilibili.com/video/av24736323/?p=62](https://www.bilibili.com/video/av24736323/?p=62)

老师微信号：creathinFeng

搭建自己的blog：[https://www.cnblogs.com/zhangqie/p/7978394.html](https://www.cnblogs.com/zhangqie/p/7978394.html)

