## vim

snipMate安装这个插件，写程序能自动补齐代码。


要粘帖的话  先进入插入模式


删除文本时，先进入可视行模式（大写的Ｖ）(此时不是插入模式时正常模式及命令模式)　ｄ删除　p粘帖( 小写大写粘帖位置不同)  ｙ是复制  <>( 整体代码缩进（＞）返回（＜）)　　

vim中可以同时打开多个buffer 看下一个用 bn 前一个用 bp   在打开一个buffer中直接打开另一个buffer用:e+b.c
退出一个buffer　用bd  

dd vim中写程序剪切某行程序代码
yy vim中粘帖刚才剪切的那段代码
p  vim中复制这段代码

##一些指令

  which git:看git 在系统下那一块
  locate vimrc:列出系统下所有的vimrc文件
  sudo updatedb:更新数据库（locate 指令的弱点：不会显示出刚刚建立的文件，所以得更新数据库，这样会解决之一弱点）
  find XXX：列出XXX中的所有内容
  find XXX | grep git(grep:字符窜)：列出XXX文件中包含字符窜git的文件“|”把前面的输出作为后面的输入
  ps aux:输出当期当前的进程，（相当于windows下的人物管理器）
  ps aux | grep firefox:查看firefox的进程号：2003
  kill 2003:可以关闭掉firefox.
  kill -9 2003:如果firefox已经死掉，这条命令可强制关掉firefox.
  XXX hello:查找含有hello的文件，e可直接进入那个文件，多个文件的上下移动j,k.
  执行make命令的前提是当前目录下必须含有makefile文件。



##git
git add file(跟踪文件)

1.创建一个文件

     _mkdir ggg

2.进入文件
 
     cd ggg 

3.初始化文件
 
     git init

4.创建文件

     ls -a

5.创建文件

     vim hello.c

6.让GIT知道这个文件

     git add hello.c

7创建第一个版本

     git commit -a -m "my first version"  (显示版本用tig)

#git 

1.git.diff     查看 guo.md和 .git(已经上传的)里面的 git.diff的区别
    
2.git reset --hard HEAD(恢复对文件的错误修改)

3.git reset --hard HEAD^(如果错误操作已经生成版本用这个操作) 

4.git revert   (如果已将生成的版本push到服务器上，用这个操作，这个操作的实际意义时先让之前的错误操作从服务器上取下来包括版本，然后再做正确的修改，重新push到服务器上，这样才能达到真正的目的，只是此时会多了两个原本没必要的版本)

5.想要删除自己笔记中的仓库  dashboard-点开不想要的项目-admin-delete this repository

6.想要删除仓库中的一个文件  在之前的目录下（git add trash）输入1.git rm trash  2.git commit -a 3.git push

7.一个文件有很多个版本 .
  
  想要回到之前的某个版本，之前的操作会显得很麻烦，git checkout + 编码（每一个版本都有编码，在tig中按d看编码，然后复制粘帖即可回到想回去的那个版本）

  想回到最新的那个版本即HEAD版本，代码是git checkout master
###打开一个标　　　ctrl + shift + t

  git branch :输出当前的分支
  返回到HEAD版本时，想要回到以前的版本，git checkout 编码 -b XXX（XXX代表新命名的一个分支名，也就是说没命名时之前回到的版本时，git branch会显示no master，如果有了这个命名，则git branch 会显示刚才命名的这个名字，git checkout master还可以回到HEAD版本，再要回去之前的那个已经命名的版本时git checkout XXX即可实现）
  
  git br -D XXX：可以删除之前命名的分支

8.一.gitk 二.qgit支持鼠标看以前的版本，（之前要安装）  
 
9.git commit -a -v:(版本中会显示此次修改的内容)



###   ｖｉｍ打开文件出现异常ｌｓ－ａ　删除这个文件（ ｒｍ－ｒｆ） .note.md.swp

##C

1. c语言学习  learn.akae.cn/media/index.html

2. 编译gcc  代码 gcc -Wall a.c(a.c为例)  Wall(警告所有) 显示结果./a.out
   编译gcc  代码 gcc -l a.c(a.c 为例)  -l后边紧跟库（去掉lib）的名字,一般都链接标准库-lc，所以一般都省略不写。
  

3. echo $?( 打印也就是输出系统返回值是多少 )"0表示没有错误"

4. :sh    这是一种编译的的代码,可以在vim未关闭的情况下直接编译，如果要改程序直接按ctrl+d可返回vim中，修改完保存完继续编译   在sh编译下vim中修改完程序并且已经保存想要返回之前的程序，u可返回，（普通模式下） ,u可返回很多步，想要前进至之前的一步，ctrl+r,  

5. 写程序，有时候修改很少代码，但需要很长的语言解释，生成的版本中只能显示很少的文字，这是在生成版本时，用git commit -a，会弹出一个vim，在这个环境下写注释，第一行会在生成的版本中显示，其余的解释不会在版本中显示enter键会显示。

6.写程序时<tab>键和空格键不能混合使用，

  o:光标在某行代码中间时，小写o可以开辟新的一行且自动补齐（正常模式下）
  ctrl-t  ctrl-d：在插入模式下，如果N行代码没有补齐，且差的不是四个空格，ctrl-t可补齐，如果多来或者是过了，ctrl-d可返回。

7.一个完整的C项目，不仅仅是一个文件，而是多个，在阅读程序时，经常会找不到定义调用，对于此类情况可以在vim中安装一个叫 ctags的程序，ctags hello.c这样会使hello.c产生一个新的文件tags然后在进入vim中读程序。如果时多文件程序，则使用这条命令（ctags *）vim全部打开.c文件，ctrl-]可以查看函数的定义ctrl-t可以返回到函数的调用

8.看一个很大的C程序时，ctrl+g直接跳到最后一页，可以看此程序有多少行，gg可以返回到最前端。

9.在C程序中会有很多个文件，有时想要该其中一个文件的名字，需要两句代码1.mv main.c hello.c2.git add *(这句代码可以全部跟踪所有文件)

# 配置文件
目前学了三个（都是隐藏文件）
1.vimrc
2.gitconfig
3.bashrc  (可设置下载代码为a，保存后，下载只需只用a即可下载，之前得全盘浏览一遍source .bashrc)
 vim .bashrc 写入alias a="sudo apt-get install"保存
source .bashrc 即可使用（foutune |cowsay为例） 
#Global setup:

 Set up git
  git config --global user.name "Your Name"
  git config --global user.email 593748946@qq.com
        

Next steps:

  mkdir my-note
  cd my-note
  git init
  touch README
  git add README
  git commit -m 'first commit'
  git remote add origin git@github.com:wsIThp/my-note.git
  git push -u origin master
      

Existing Git Repo?

  cd existing_git_repo
  git remote add origin git@github.com:wsIThp/my-note.git
  git push -u origin master
      

Importing a Subversion Repo?

  Click here
      

When you're done:

  Continue

