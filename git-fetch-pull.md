git fetch是将远程主机的最新内容拉到本地，检查之后用户决定是否合并到工作本机分支中。

git pull 则是将远程主机的最新内容拉下来后直接合并，即：git pull = git fetch + git merge


```bash
#这个命令将某个远程主机的更新全部取回本地
$ git fetch <远程主机名> 

#取回特定分支的更新 注意之间有空格
$ git fetch <远程主机名> <分支名> 
```
