首先打开Git Bash软件，再进入所创建的文件中

![alt text](<屏幕截图 2025-08-07 205940.png>)
![alt text](<屏幕截图 2025-08-07 205946.png>)

### sgyr@SG□ķ□□□ MINGW64 /d/self_learning
$ git clone https://github.com/SG830/self-learning.git
Cloning into 'self-learning'...
remote: Enumerating objects: 34, done.
remote: Counting objects: 100% (34/34), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 34 (delta 9), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (34/34), 1.77 MiB | 3.39 MiB/s, done.
Resolving deltas: 100% (9/9), done.

- git clone将https://github.com/SG830/self-learning.git地址对应的远程github仓库克隆到本地d盘下的self_learning
  
### sgyr@SG□ķ□□□ MINGW64 /d/self_learning
$ ls
self-learning/

- ls 显示当前目录下的文件
  
### sgyr@SG□ķ□□□ MINGW64 /d/self_learning
$ cd self-learning/

- 进入到d盘中的self_learning文件夹中的self-learning即进入仓库
- cd self-learning/ 和 cd self-learning 有什么区别？​
  - / 表示这是一个​​目录路径​​，**更明确地告诉系统这是一个文件夹（而不是文件）**
  - 在自动补全时，系统通常会自动加上 /（比如按 Tab 键补全时）
  - cd self-learning也能正常进入文件夹，但系统会先检查 self-learning 是文件还是文件夹，如果同名文件存在（比如 self-learning 是个文本文件），会报错

### sgyr@SG□ķ□□□ MINGW64 /d/self_learning/self-learning (main)
$ ls
 7.20笔记.docx            note.md    Python/                   Python运算.docx
'7.23markdown 教程.pdf'   note.pdf   Python的条件和循环.docx   README.md

- 显示了了github 仓库中已经有的文件
- cd​​ 是 ​​"Change Directory"（切换目录）​​ 的缩写，用于在命令行中进入或退出文件夹
  
### sgyr@SG□ķ□□□ MINGW64 /d/self_learning/self-learning (main)
$ vi testing.txt

- 用vim编辑器创建新文件

### sgyr@SG□ķ□□□ MINGW64 /d/self_learning/self-learning (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

==Untracked files:==
  (use "git add <file>..." to include in what will be committed)
        testing.txt

nothing added to commit but untracked files present (use "git add" to track)

- ​​git status查看文件状态，Untracked files表示新文件未被Git追踪

### sgyr@SG□ķ□□□ MINGW64 /d/self_learning/self-learning (main)
$ git add testing.txt
warning: in the working copy of 'testing.txt', LF will be replaced by CRLF the next time Git touches it

- 将文件加入暂存区（准备提交）

### sgyr@SG□ķ□□□ MINGW64 /d/self_learning/self-learning (main)
$ git commit -m "testing"
[main 1bfdf3f] testing
 1 file changed, 1 insertion(+)
 create mode 100644 testing.txt

- 将暂存区文件打包为一个版本，-m后的引号内必须写提交说明例如：时间，修改的2.0版本等描述

### sgyr@SG□ķ□□□ MINGW64 /d/self_learning/self-learning (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 272 bytes | 272.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/SG830/self-learning.git
   cb0366a..1bfdf3f  main -> main

- 将本地提交推送到GitHub




# 只需这3步即可更新仓库
git add .（.表示全部文件，添加当前目录下的所有文件​ 到 Git 的暂存区（准备提交））
git commit -m "描述修改内容"
git push