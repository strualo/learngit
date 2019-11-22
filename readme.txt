 git init　　//把这个目录变成Git可以管理的仓库
git add README.md　　 //文件添加到仓库　git add　. 一个点就把当前目录下所有未追踪的文件全部add了 
git commit -m "first commit"
git remote add origin git@github.com:strualo/a.git　 //关联远程仓库 地址需要修改
git push -u origin master //把本地库的所有内容推送到远程库上


git log
git reflog              #找到相应的 HEAD；
git reset --hard  XXXX  #通过 reset 命令恢复，其中最后的 XXXX 是 HEAD 的地址


git pull origin master 
git clone


二、管理分支
1、查看分支
查看本地分支
使用 git branch命令，如下： git branch
master
*标识的是你当前所在的分支。

查看远程分支
命令如下：git branch -r

查看所有分支  命令如下：git branch -a


2、本地创建新的分支
命令如下：  git branch [branch name]
例如： git branch gh-dev

3、切换到新的分支
命令如下：git checkout [branch name]
例如：$ git checkout gh-dev
Switched to branch 'gh-dev'

4、创建+切换分支
创建分支的同时切换到该分支上，命令如下：git checkout -b [branch name]

git checkout -b [branch name] 的效果相当于以下两步操作：
git branch [branch name]
git checkout [branch name]

5、将新分支推送到github
命令如下：git push origin [branch name]

例如：git push origin gh-dev

6、删除本地分支
命令如下：git branch -d [branch name]
例如：git branch -d gh-dev

7、删除github远程分支
命令如下：git push origin :[branch name]
分支名前的冒号代表删除。
例如：git push origin :gh-dev



git rm <file>
git rm -f <file>  #强制删除，git add 之后只能强制删除，工作区和缓存区一起删除
git rm --cached <file>  #从git的缓存区删除，工作区的文件会保留，实测好像和移出版本管理是一个效果
git rm –r *  # 递归删除


