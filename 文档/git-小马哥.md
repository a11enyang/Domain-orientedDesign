# git

网站：try.git.io

### 1.系统开发流程

1. 编写代码
2. 提交代码给git本地库
3. 提交代码给git远程库，分享给团队其他人
4. 从远程库中获取最新代码
5. 继续修改编写代码
6. 重复第二步以后的操作



### 2.git概念

1. 本地工作文件夹
2. git索引区（stage）
3. git库（respository）
   1. 本地库
   2. 远程库（服务器端）



### 3.git的基础设定

```bash
$ git init 将当前文件夹作为git的本地文件夹
$ git config -l 查看当前设置
$ git config --global user.name "yangweidong"
$ git config --global user.eamil "yangweidong2qq.com"
$ git config --global color.ui true 
```



### 4.方便的命令

```bash
git config --help
```



### 5.第一次提交

##### 1. 知识点

*建立文件（本地文件夹）

*追加文件（索引区）

*提交文件（本地库）



##### 2.练习

```bash
$ git status 查看git状态
$ git add file 将本地文件夹的文件添加到索引区
$ git commit 将索引区的内容添加到本地库
$ git log 查看提交历史
```

设置显示中文：

```bash
$ git config --global core.quotepath false
```





### 6.查看提交履历

```bash
$ git log 
$ git log --online
```



### 7.把握git的状态

```txt
红色：表示存在当前文件夹中，没有add到索引区， 表示没有保存
绿色： 表示存在索引区中，没有commit到本地库中
```

```bash
git status
git checkout -- file 取消将文件存入索引区的操作
```



### 8.比较修改内容

 ```bash
git diff 比较本地文件夹与本地库保存的文件的不同
git diff --cached 比较索引区与本地库保存的文件的不同啊
 ```

![image-20200325171704565](./note.assets/image-20200325171704565.png)

链接：https://blog.csdn.net/Jeffxu_lib/article/details/86589070

### 9.文件操作

```bash
$ git mv file1 file2 可以用于移动文件夹，也可以用于对于文件的重命名
$ git rm --cached file 删除索引区的文件
```



### 10.忽略版本管理

在git的根目录文件夹下面，添加.gitignore文件，这个文件是需要进行版本管理的

打开.gitignore文件，然后输入输入想要忽略的文件



### 11.更新最后的提交

将这次的提交添加到上一次的提交中，还是使用同样的comment

```bash
git commit --amend
```



### 12.返回过去







### 13.分支问题

![image-20200325210052875](./note.assets/image-20200325210052875.png)

从master分支中建立了一个新的分支，并且在主分支和feature分支上都有了新的提交



```bash
git branch //查看当前分支的情况，*表示当前正在使用的分支
```





### 14.git rebase

![image-20200325212254173](./note.assets/image-20200325212254173.png)

在本地创建两个分支，一个是master，一个是my_cool_fearure

1. 切换到master分支上

```bash
git checkout -b master
```

然后获取同事的内容

![image-20200325212716271](./note.assets/image-20200325212716271.png)

```bash
git pull
```

2. 切换到自己的工作目录

```bash
git checkout -b my_cool_feature
```

进行变基操作

```bash
git rebase master
```

![image-20200325213032092](./note.assets/image-20200325213032092.png)



3. 然后切换到master目录

   进行变基操作

   ```
   git rebase my_cool_feature
   ```

   ![image-20200325213317962](./note.assets/image-20200325213317962.png)

4. 最后提交内容

   ```bash
   git pull
   ```

   

### 15.git merge

将 master 分支合并到 feature 分支最简单的办法就是用下面这些命令：

```
git checkout feature
git merge master
```

或者，你也可以把它们压缩在一行里。

```
git merge master feature
```

feature 分支中新的合并提交（merge commit）将两个分支的历史连在了一起。你会得到下面这样的分支结构：

![image-20200325223126669](./note.assets/image-20200325223126669.png)

https://github.com/geeeeeeeeek/git-recipes/tree/master/sources



### 16.仓库的创建

1. 需要先生成ssh密钥，然后将rsa.pub添加到github的设置中
2. 在github中创建一个仓库
3. 然后直接在终端中进行clone