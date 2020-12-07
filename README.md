Git Command
--- 

### 新建代码库

```bash
#在当前目录新建一个Git代码库
$ git init 

# 新建一个目录，将其初始化为Git代码库
$ git init [project-name]

# 下载一个项目和它的整个代码历史
$ git clone [url]
```

### 配置
```bash
# 显示当前的Git配置
$ git config --list

# 编辑Git配置文件
$ git config -e [--global]

# 设置提交代码时的用户信息
$ git config [--global] user.name "[name]"
$ git config [--global] user.email "[email address]"

# 忽略文件配置
$ touch .gitignore

# 移除指定文件跟踪状态(忽略文件失效时使用)
$ git rm -r --cached [file]

```
##### 忽略文件一览:[ https://gitee.com/jaywcjlove/oscnews/releases](https://gitee.com/jaywcjlove/oscnews/releases)

##### Git 忽略规则匹配语法
在 .gitignore 文件中，每一行的忽略规则的语法如下：

空格不匹配任意文件，可作为分隔符，可用反斜杠转义
- #` 开头的模式标识注释，可以使用反斜杠进行转义
- ! 开头的模式标识否定，该文件将会再次被包含，如果排除了该文件的父级目录，则使用!也不会再次被包含。可以使用反斜杠进行转义
- / 结束的模式只匹配文件夹以及在该文件夹路径下的内容，但是不匹配该文件。/ 开始的模式匹配项目跟目录。如果一个模式不包含斜杠，则它匹配相对于当前 .gitignore 文件路径的内容，如果该模式不在 .gitignore 文件中，则相对于项目根目录
- ** 匹配多级目录，可在开始，中间，结束
- ? 通用匹配单个字符
- [] 通用匹配单个字符列表


### 增加/删除文件
```bash
# 添加指定文件到暂存区
$ git add [file1] [file2] ...

# 添加指定目录到暂存区，包括子目录
$ git add [dir]

# 添加当前目录的所有文件到暂存区
$ git add .

# 添加每个变化前，都会要求确认
# 对于同一个文件的多处变化，可以实现分次提交
$ git add -p

$ Stage this hunk [y,n,q,a,d,/,s,e,?]?

y - 暂存此区块
n - 不暂存此区块
q - 退出；不暂存包括此块在内的剩余的区块
a - 暂存此块与此文件后面所有的区块
d - 不暂存此块与此文件后面所有的 区块
g - 选择并跳转至一个区块
/ - 搜索与给定正则表达示匹配的区块
j - 暂不决定，转至下一个未决定的区块
J - 暂不决定，转至一个区块
k - 暂不决定，转至上一个未决定的区块
K - 暂不决定，转至上一个区块
s - 将当前的区块分割成多个较小的区块
e - 手动编辑当前的区块
? - 输出帮助

# 删除暂存区的文件
$ git restore --staged [file]

# 删除工作区文件，并且将这次删除放入暂存区
$ git rm [file1] [file2] ...

# 停止追踪指定文件，但该文件会保留在工作区
$ git rm --cached [file]

# 改名文件，并且将这个改名放入暂存区
$ git mv [file-original] [file-renamed]
```

### 代码提交
