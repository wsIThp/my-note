mynote


## vim


要粘帖的话  先进入插入模式


##git
git add file(跟踪文件)

1创建一个文件夹
 mkdir ggg

2进入文件 
cd ggg 

3初始化文件 
git init

创建文件
 ls -a

5创建文件
 vim hello.c

6让GIT知道这个文件
 git hello.c

7创建第一个版本
 git commit -a -m "my first version"  (显示版本用tig)




Global setup:

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

