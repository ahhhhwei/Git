# Git 与 Git 安装

## 一、版本控制器

我们在编写各种⽂档时，为了防⽌⽂档丢失，更改失误，失误后能恢复到原来的版本，不得不复制出副本，基于副本进行改动。但是，**随着版本数量的不断增多，我们不记得每个版本都做了哪些修改。**

**解决方案：**

为了能够更⽅便我们管理这些不同版本的⽂件，便有了版本控制器。所谓的版本控制器，就是能让你了解到⼀个⽂件的历史，以及它的发展过程的系统。通俗的讲就是⼀个可以记录⼯程的每⼀次改动和版本迭代的⼀个管理系统，同时也⽅便多⼈协同作业。

- ⽬前最主流的版本控制器就是 Git 。Git 可以控制电脑上所有格式的⽂件。
- 所有的版本控制系统，只能跟踪文本文件的改动。
  - 比如 TXT 文件，网页，所有的程序代码等等。版本控制系统可以告诉你每次的改动，比如在第5行加了一个单词 “Linux”，在第8行删了一个单词 “Windows”。
  - 而图片、视频这些二进制文件，虽然也能由版本控制系统管理，但没法跟踪文件的变化，只能把二进制文件每次改动串起来，也就是只知道图片从100KB改成了120KB，但到底改了啥，版本控制系统不知道，也没法知道。

## 二、Git 安装

### 1.centos 系统

1. 查看系统是否安装了 Git：

   ```shell
   git --version
   ```

   ```shell
   bash: git: command not found...
   ```

2. 安装 Git：

   ```shell
   yum install git -y
   ```

   ```shell
   Loaded plugins: fastestmirror, langpacks
   Loading mirror speeds from cached hostfile
   Resolving Dependencies
   --> Running transaction check
   ---> Package git.x86_64 0:1.8.3.1-25.el7_9 will be installed
   --> Processing Dependency: perl-Git = 1.8.3.1-25.el7_9 for package: git-1.8.3.1-25.el7_9.x86_64
   --> Processing Dependency: perl(Term::ReadKey) for package: git-1.8.3.1-25.el7_9.x86_64
   --> Processing Dependency: perl(Git) for package: git-1.8.3.1-25.el7_9.x86_64
   --> Processing Dependency: perl(Error) for package: git-1.8.3.1-25.el7_9.x86_64
   --> Running transaction check
   ---> Package perl-Error.noarch 1:0.17020-2.el7 will be installed
   ---> Package perl-Git.noarch 0:1.8.3.1-25.el7_9 will be installed
   ---> Package perl-TermReadKey.x86_64 0:2.30-20.el7 will be installed
   --> Finished Dependency Resolution
   
   Dependencies Resolved
   
   =======================================================================================
    Package                 Arch          Version                    Repository      Size
   =======================================================================================
   Installing:
    git                     x86_64        1.8.3.1-25.el7_9           updates        4.4 M
   Installing for dependencies:
    perl-Error              noarch        1:0.17020-2.el7            base            32 k
    perl-Git                noarch        1.8.3.1-25.el7_9           updates         56 k
    perl-TermReadKey        x86_64        2.30-20.el7                base            31 k
   
   Transaction Summary
   =======================================================================================
   Install  1 Package (+3 Dependent packages)
   
   Total download size: 4.5 M
   Installed size: 22 M
   Downloading packages:
   (1/4): perl-Error-0.17020-2.el7.noarch.rpm                      |  32 kB  00:00:00     
   (2/4): perl-Git-1.8.3.1-25.el7_9.noarch.rpm                     |  56 kB  00:00:00     
   (3/4): perl-TermReadKey-2.30-20.el7.x86_64.rpm                  |  31 kB  00:00:00     
   (4/4): git-1.8.3.1-25.el7_9.x86_64.rpm                          | 4.4 MB  00:00:00     
   ---------------------------------------------------------------------------------------
   Total                                                     7.3 MB/s | 4.5 MB  00:00     
   Running transaction check
   Running transaction test
   Transaction test succeeded
   Running transaction
     Installing : 1:perl-Error-0.17020-2.el7.noarch                                   1/4 
     Installing : perl-TermReadKey-2.30-20.el7.x86_64                                 2/4 
     Installing : git-1.8.3.1-25.el7_9.x86_64                                         3/4 
     Installing : perl-Git-1.8.3.1-25.el7_9.noarch                                    4/4 
     Verifying  : 1:perl-Error-0.17020-2.el7.noarch                                   1/4 
     Verifying  : git-1.8.3.1-25.el7_9.x86_64                                         2/4 
     Verifying  : perl-Git-1.8.3.1-25.el7_9.noarch                                    3/4 
     Verifying  : perl-TermReadKey-2.30-20.el7.x86_64                                 4/4 
   
   Installed:
     git.x86_64 0:1.8.3.1-25.el7_9                                                        
   
   Dependency Installed:
     perl-Error.noarch 1:0.17020-2.el7           perl-Git.noarch 0:1.8.3.1-25.el7_9      
     perl-TermReadKey.x86_64 0:2.30-20.el7      
   
   Complete!
   ```

### 2.ubuntu 系统

1. 查看系统是否安装了 Git：

   ```shell
   git --version
   ```

2. 安装 Git：

   ```shell
   apt-get install git -y
   ```

   