### DEMO001

## 注意切记备份之前修改的记录

使用场景：用于提交到远端后需要覆盖其记录（只能覆盖之前一次提交）

```bach
# 将当前版本重置到需要重置的版本之前的第一个版本
$ git reset --hard b054f9fa607e83a060a343437f40edc20d66e482
```

将修改的文件重新修改

```bach
# 添加到暂存区
$ git add .
```

```bach
# 提交到本地仓库
$ git commit -m "message"
```

```bach
# 强制覆盖其提交记录
$ git push origin duanzhigang --force
```
