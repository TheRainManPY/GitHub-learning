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
- 5.merge branch with no-ff
    + 1）git merge --no-ff -m'合并分支并不使用Fast forward模式' <branchname>
    + 2）采用ff模式的合并是把master的指针指到dev的最新commit上，所以这两个分支的最新commit_id是一样的。但采用--no-ff模式合并分支，由于不能把master的指针直接指向dev分支的最新commit，master分支只能进行一次提交操作，所以就会有内容一模一样，commit_id不同的情况。
- 5.save work status
    + 1）git stash 保存当前工作，未commit，已add的工作内容
    + 2）git stash list 查看保存的工作进度
    + 3）git stash apply stash@{index}恢复指定
    + 4）git stash drop/git stash pop删除
    + 5）这类似于一个list？
