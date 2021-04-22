## Git 命令
```shell
git init // 初始化一个控制的git仓库
git clone "git的克隆地址" // 克隆git项目

git clone "git的克隆地址" -b "branch"// 克隆git项目的branch分支

git config --list --show-origin //查看Git配置所在的文件
git config --global user.name "John Doe" //设置全局提交时的用户名 这个很重要
git config --global user.email johndoe@example.com //设置全局提交时的邮件 这个很重要

// git add
git add *.txt //git添加目录和子目录下所有.txt结尾的文件
git add .\testFile\    // git 添加testFile目录下所有文件 
git add .\Git学习笔记.md // git添加单独的一个文件
git commit -m 'initial project version' // 提交到本地;'initial project version'为提交信息

git status //查看当前的文件状态
git status -s  //查看当前的文件状态,显示的更精简

git log //查看提交历史
git log -p // 查看提交的差异
git log -p -2 //查看最近2次的提交差异
git --stat //每次提交的下面列出所有被修改过的文件、有多少文件被修改了以及被修改过的文件的哪些行被移除或是添加了。 在每次提交的最后还有一个总结
//替换提交
$ git commit -m 'initial commit'
$ git add forgotten_file
$ git commit --amend // 第二次提交将代替第一提交的结果


```

## Git概念

- Git 有三种状态，你的文件可能处于其中之一： 已提交（committed）、已修改（modified） 和 已暂存（staged）
- 已修改表示修改了文件，但还没保存到数据库中。

- 已暂存表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。

- 已提交表示数据已经安全地保存在本地数据库中。



工作目录下的每一个文件都不外乎这两种状态：已跟踪 或 未跟踪
- 已跟踪的文件是指那些被纳入了版本控制的文件;
- 工作目录中除已跟踪文件外的其它所有文件都属于未跟踪文件

### Git 忽略文件格式规范
文件 .gitignore 的格式规范如下：

所有空行或者以 # 开头的行都会被 Git 忽略。

可以使用标准的 glob 模式匹配，它会递归地应用在整个工作区中。

匹配模式可以以（/）开头防止递归。

匹配模式可以以（/）结尾指定目录。

要忽略指定模式以外的文件或目录，可以在模式前加上叹号（!）取反。