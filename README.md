# GitHub-learning
### 学习GIT
#### Git配置相关
- 1.key
    + 1）生成key使用的email应该与使用的github(帐号)相同
    + 2）push commit时git config user.name/email 设置的是提交的用户(github帐号)
    + 3）privatekey应该使用ssh-add ~/.ssh/xxx 添加到ssh.keys列表中，可以使用ssh-add -l 命令查看已经添加的key
- 2.publickey
    + 1）用哪个邮箱生成的key对应哪个github(email)帐号提交

#### Git branch相关
- 1.create branch
    + 1）git checkout -b dev 创建dev分支并切换到dev
    + 2）git branch 查看project中所有分支
- 2.delete branch
    + 1）git branch -d <branchname>
- 3.merge branch
    + 1）*master: git merge <branchname>
- 4.watch branch merge
    + 1）git log --graph
- 5.save work status
    + 1）git stash 保存当前工作，未commit，已add的工作内容
    + 2）git stash list 查看保存的工作进度
    + 3）git stash apply stash@{index}恢复指定
    + 4）git stash drop/git stash pop删除
    + 5）这类似于一个list？
- 6.多人协作
    + 1）可以直接 git clone git@github.com:xxxx/xxxx
    + 2）也可以创建本地仓库后使用 git remote add origin git@github.com:xxxx/xxxx 添加远程库地址
    + 3）上面两种方法都只会同步下来master分支，若要同步其他分支需使用：git checkout -b <branchname> origin/<branchname> 在本地创建和远程分支对应的分支
    + 4）再gitpull同步远程分支，若出现no tracking information，则说明本地分支和远程分支的链接关系没有创建，使用：git branch --set-upstream <branchname> origin/<branch-name>
