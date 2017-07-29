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
    + git log --graph

