# Git源码管理

## Git基本指令
*安装Git*
- sudo apt-get install git

*创建版本库*
 1. 先要创建一个目录, 这个目录就是用来存放仓库的
    - $ mkdir html
    - $ cd html
 
 2. 使用git init命令, 将当前目录创建成git仓库.
    - $ git init
    
 *增加文件*
  1. 当前目录里没有文件, 那么我们先创建一个文件README
     - $ touch README
  
  2. 编辑这个文件, 写一点东西在里面.
     - $ vim README
     
  3. 先用查看当前状态的命令, 查看一下现在目录下文件的状态.
     - $ git status
     
  4. 把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化.
     - $ git add README
     
  5. 现在使用查看状态的命令, 看一下是目录下文件的状态.
     - $ git status
     
  *提交*
   - $ git commit
   
  *配置用户信息*
   1. 配置用户名
      - $ git config --global user.name
   
   2. 配置用户邮箱
      - $ git config --global user.email
      
   3. 配置编辑提交信息的编辑器
      - $ git config --global core.editor vim
   
  *查看提交信息*
   - $ git log
    
## Git远程仓库

  *添加远程仓库*
   1. 如果我们现在本地有一个git仓库, 我们使用remote add 命令将它添加到远程的仓库中.
      - $ git remote add origin https://github.com/wangleihd/h5class.git
      
   2. 并需要将远程的仓库的信息更步到本地, 这里主要指的示远程仓库的分支和远程库的提交变更信息.
      - $ git fetch origin
      
  *从远程仓库上同步*
  
     *clone*
      - 当我们知道git仓库的地址了(在github上有很多的开源仓库.), 就可以使用下面的命令将源码拉取到本地
        - $ git clone url
      
     *pull*
      - 我们已经拉取源码到本地了, 但是服务器上的git已经更新了, 当我们需要将服务器的源码与本地源友进行同步进时, 需要使用下面的命令.
        - $ git pull
