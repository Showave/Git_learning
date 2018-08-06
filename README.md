# Git_learning
learning for Git
1. 初始化一个Git仓库，使用git init命令
2. 添加文件到Git仓库，分两步：
         a. 使用命令git add <file>，注意，可反复多次使用，添加多个文件；
         b. 使用命令git commit -m <message>，完成。
3. 要随时掌握工作区的状态，使用git status命令.如果git status告诉你有文件被修改过，用git diff可以查看修改内容。
4. HEAD指向的版本就是当前版本，使用命令切换版本： git reset --hard commit_id.     HEAR^ #上个版本，^^上两个版本
          git log   #查看提交历史          git reflog # 查看命令历史
5.git add命令实际上就是把要提交的所有修改放到暂存区（Stage），然后，执行git commit就可以一次性把暂存区的所有修改提交到分支。
6. git diff HEAD -- readme.txt命令可以查看工作区和版本库里面最新版本的区别
7. a. 直接丢弃工作区的修改时，用命令git checkout -- file。
    b. 改乱工作区，还添加到了暂存区时，想丢弃修改，第一步用git reset HEAD <file>，就回到了a，第二步按a操作.
8. git rm test.txt    -> $ git commit -m "remove test.txt"
    git checkout -- test.txt ##还原
9.  要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
     关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

     此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

10. 要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆。

     Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。

11. 

Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

12. 用git log --graph命令可以看到分支合并图。

BUG分支

















