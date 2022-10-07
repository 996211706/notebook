# Git 学习笔记
## 一、初识 Git
1. Git 下载和安装
- 上 https://git-scm.com/ 网站下载 Git。
- 安装 Git (一路 next) ，装完出现 Git bash 以及右键出现 `Git GUI Here` 和 `Git Bash Here` 两个选项。
<div align=center><img src="/screenshot-01.png" width="30%"></div>

- 其中 Git Bash 是弹出一个类似于 DOS 的 MinGW64 指令窗。<div align=center><img src="/screenshot-02.png" width="80%"></div>和 DOS 一样，默认位置是在 C 盘的用户目录下，想要切换位置的话就用 `cd` 指令。如果在文件管理器中的某个目录下右键点击 `Git Bash Here` 选项，则它也会弹出一个指令窗，并且该指令窗的位置直接就是在当前目录下。

2. 认识 Github/GitLab
- 以上两个都是网页端的 Git 仓库管理平台，属于是远程管理端口，可以和本地仓库交换数据/源码，例如在 Git bash 窗口中使用 `remote add` 以及 `push`, `clone` 等指令。

3. Git 仓库(**repository**)
+ *Git仓库*，又称*Git版本库*，就是所谓的`Repository`，它储存着所有可以通过Git来进行管理的文件。Git仓库分为远程仓库和本地仓库两种：
  - 远程仓库存储在Github/GitLab上面，可以进行线上管理；
  - 本地仓库存储在用户本地的计算机磁盘上，可以通过Git Bash来进行管理。

4. 本地Git配置
- 在进行本地Git仓库的创建与管理之前，我们必须现在Git客户端中注册一个属于自己的用户名和邮箱，来代表自己的身份。这样在每次进行操作的时候Git会把你记录下来，以后查询历史的时候就能够知道谁对仓库进行过操作了。
    + 配置用户名邮箱的方法：在`Git Bash`中输入如下两行指令
        ```
        git config --global user.name 用户名
        git config --global user.email 邮箱
        ```
        其中`用户名`和`邮箱`自己按需填写，不需要加引号。
- 其他git的配置信息可以通过如下指令进行查看：
    ```
    git config --list
    ```
    输出结果如下：
    <div align=center><img src="/screenshot-06.png" width="80%"></div>

    （最后输入`:q`退出编辑模式。）

5. 创建第一个仓库
- 本地创建仓库的方法通常是先选择你仓库所在的目录，然后右键打开 `Git Bash` 来进行创建，指令是：
    ```
    git init
    ```
    输出结果如下：
    <div align=center><img src="/screenshot-03.png" width="80%"></div>
    
    并且在该目录下出现一个叫`.git`的隐藏文件夹，<div align=center><img src="/screenshot-04.png" width="80%"></div>
    
    就说明你创建成功了。此外，可以在Git Bash命令行里面输入
    ```
    git status
    ```
    输出结果如下：
    <div align=center><img src="/screenshot-05.png" width="80%"></div>

    该命令可以用来查看你Git仓库的状态。
## 二、Git 入门操作
1. 学习 Git 代码 (vim, add, commit)
2. Git 分支结构
3. 提交与修改
4. 上传至 Github/GitLab（http方式）
5. SSH 加密
6. 上传至 Github/GitLab（SSH方式）