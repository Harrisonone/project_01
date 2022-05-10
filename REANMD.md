# github的基本使用
## git的基本操作
1.git init在现有目录中进行初始化管理仓库

2.git status检查文件当前所处的状态  出现红色显示的样式表示以下文件未被跟踪。

3.git add 名称.index 开始跟踪一个文件 添加成功后，进行git status查看当前文件状态，出现绿色标志则说明添加该文件至暂存区。

4.精简版直接显示文件当前所处的文件状态，命令如下
git status -s.

5.清空Bash当前所显示的文件内容  clear

6.提交更新 现在暂存区有一个index.html文件等待被提交到git仓库中进行保存。执行git commit 命令进行提交，其中-m 选项是显示后面提交的消息，用来对提交信息进行一些描述 eg：
git commit -m "新建了index.html文件"。之后可以通过git status查看当前文件状态。

7.暂存已修改的文件，继续使用git add index.html进行缓冲添加。执行git commit 命令进行提交，变更为最新的代码内容。

8.撤销对文件的修改 还原成git仓库所保存的版本。！！！操作的结果是：所有的修改都会丢失，且无法恢复！执行语句：git checkout -- index.html

9.向暂存区里面添加多个文件 git add . 一次性将修改或原有的文件添加至暂存区

10.取消暂存文件 从暂存区中移除对应的文件 git reset HEAD 要移除的文件名称  一次性全部移除则为 git reset HEAD .

11.跳过使用暂存区 直接将工作区的修改提交到git仓库里 git commit -a -m "描述消息"

12.移除文件【（1）git仓库和工作区同时移除对应的文件 git rm -f index.js  （2）只从git仓库中移除，保留工作区对应的文件
git rm --cached index.css】

13.忽略文件 创建一个名为gitignore的配置文件
> 1. 以#开头的是注释
> 2. 以/结尾的目录
> 3. 以/开头防止递归
> 4. 以！开头表示取反
> glob模式匹配

14.查看提交历史 
> git log 查看完整的提交历史 git log --pertty==oneline
> git log -2 查看最近两次提交的历史



