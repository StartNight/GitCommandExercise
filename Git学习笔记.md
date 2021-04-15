## Git 命令
```shell
git init // 初始化一个控制的git仓库
git clone "git的克隆地址" // 克隆git项目

git clone "git的克隆地址" -b "branch"// 克隆git项目的branch分支

git config --list --show-origin //查看Git配置所在的文件
git config --global user.name "John Doe" //设置全局提交时的用户名 这个很重要
git config --global user.email johndoe@example.com //设置全局提交时的邮件 这个很重要


```

## Git概念

- Git 有三种状态，你的文件可能处于其中之一： 已提交（committed）、已修改（modified） 和 已暂存（staged）
- 已修改表示修改了文件，但还没保存到数据库中。

- 已暂存表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。

- 已提交表示数据已经安全地保存在本地数据库中。
