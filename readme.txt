2.
git clone learngit
git cheackout -b dev origin/dev
git switch -c dev origin/dev

3.
git pull --rebase
git merge

4.
git revert -n version_number

5.
git cheackout master
git merge feature-1
git commit
git push

6.
git tag -a v0.1 -m "version 0.1 released" [commit id]
git push origin v0.1

git tad -d v0.9
git push origin :refs/tags/v0.9

7.

git stash
git checkout dev 
git pull
git merge
git commit
git push
git checkout master
git cherry-pick [bug commit id]
git checkout feature-1
git stash pop

8.
git log --author="cheny" --after="2020.04.02" --before="2020.08.06" --pretty=oneline --abbrev-commit

9.
git reset 01e31c

10.

git rebase -i HEAD~5
应该吧HEAD~N中的N设置的大些，一次性把错误的提交都包含，通过一次rebase完成修改
 
11.
git merge和git rebase一样都是用于从一个分支获取并且合并到当前分支，merge是把目标分支合并到当前分支，rebase是把两个分支“变基”，成一个长的分支。

12.
都是从远程拉取代码到本地，git fetch只是拉取到本地，git pull不仅拉取到本地还merge到本地分支中。所以git pull是git fetch与git merge的集合体。git full --rebase 是git pull之后再变基

13.
工作区是当前电脑本地的工作环境，暂存区是本地文件commit之后存储的区域，版本库是远程仓库

14
git checkout -b feature origin/feature
git add .
git pull --rebase
git commit
git push