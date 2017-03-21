git新建分支命令：git branch dev(分支名dev)

git切换分支命令：git checkout dev(切换到dev分支)

以上两条命令相当于：git checkout -b dev(新建dev分支并切换到dev分支)

git branch 查看当前分支（列出所有分支，当前分支会有*号）

在dev分支修改内容并提交

	git add a.txt 
	git commit -m "修改内容"

然后切换回master分支

	git checkout master

然后发现a.txt没有变化，因为刚才提交到的是dev分支，现在切回了master分支

接下来将dev分支合并到master分支

	git merge dev   (git merge命令用于合并指定(dev)分支到当前分支(master))

合并到master分支后，dev分支就可以删除了
	
	git branch -d dev  (删除dev分支)

Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

$ git merge feature1
Auto-merging a.txt
CONFLICT (content): Merge conflict in a.txt
Automatic merge failed; fix conflicts and then commit the result.


我现在切换回master分支目的是想演示解决冲突

创建了新的分支 feature1，并插入了一行
git checkout -b feature1
git add a.txt
git commit -m "又创建切换到了feature1分支，并修改了内容"


再次切换到master分支
git checkout master

再次合并feature1分支到master分支
git merge feature1

添加远程库
git remote add origin 远程仓库地址

把本地库的内容推送到远程库
git push -u origin master (将当前分支master推送到远程库，第一次推送时远程库是空的，所以加了 -u 参数)

以后再次推送到远程库时只需要
git push origin master














