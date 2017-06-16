# Linux基本指令的使用

## 文本编辑器Vim的基本使用
 *vim的基本使用* 
- i：在当前字符的左边插入
- I：在当前行首插入
- a：在当前字符的右边插入
- A：在当前行尾插入
- o：在当前行下面插入一个新行
- O：在当前行上面插入一个新
- h: 向前移动一个字符
- j: 向上移动一行
- k: 向下移动一行
- l: 向后移动一个字符
- yy: 复制当前一行
- dd:剪切当前一行
- p: 粘贴内容到游标之后
- P: 粘贴内容到游标之前

## Linux文件系统
 *基本的文件操作*
 1. 文件的创建、删除、复制、重命名、移动
 - touch  file
 - cp file file1
 - cp file  /home/linux/file1
 - mv file   file2
 - mv file  /home/linux/
 2. 列出文件列表
 - ls -al
 3. 查看文件内容
 - cat file
 
 *基本的目录操作*
 1. 目录的创建、删除、复制、重命名、移动
 - mkdir dir
 - cp dir   dir1  -a
 - cp dir   /home/linux/dir2  -a
 - mv dir  dir2
 - mv dir  /home/linux/
 - rm  dir  -rf
 2. 列出目录列表
 - ls -d  dir
 3. 目录中查找文件
 - find  ./dir  -name  "filename"

