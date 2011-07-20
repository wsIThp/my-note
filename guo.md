mynote


## vim


要粘帖的话  先进入插入模式


删除文本时，先进入可视行模式（大写的Ｖ）(此时不是插入模式时正常模式及命令模式)　ｄ删除　p粘帖( 小写大写粘帖位置不同)  ｙ是复制  <>( 整体代码缩进（＞）返回（＜）)　　

vim中可以同时打开多个buffer 看下一个用 bn 前一个用 bp   在打开一个buffer中直接打开另一个buffer用:e+b.c
退出一个buffer　用bd  





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

     git hello.c

7创建第一个版本

     git commit -a -m "my first version"  (显示版本用tig)

#git 

1.git.diff     查看 guo.md和 .git(已经上传的)里面的 git.diff的区别
    
2.git reset --hard HEAD(回复对guo.md的修改)

3.git reset --hard HEAD^(如果已经生成版本用这个操作) 

###打开一个标　　　ctrl + shift + t





###   ｖｉｍ打开文件出现异常ｌｓ－ａ　删除这个文件（ ｒｍ－ｒｆ） .note.md.swp

##C

1. c语言学习  learn.akae.cn/media/index.html

2. 编译gcc  代码 gcc -Wall a.c(a.c为例)  Wall(警告所有) 显示结果./a.out

3. echo $?( 打印也就是输出系统返回值是多少 )"0表示没有错误"

4. :sh    这是一种编译的的代码,可以在vim未关闭的情况下直接编译，如果要改程序直接按ctrl+d可返回vim中，修改完保存完继续编译   在sh编译下vim中修改完程序并且已经保存想要返回之前的程序，u可返回，（普通模式下） ,u可返回很多步，想要前进至之前的一步，ctrl+r,  

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

