# Installation

## 本環境インストールコマンド一覧

Python2.6.6(標準でインストールされている可能性あり)

    $ yum -y install python  

Python2.7

    $ yum -y install centos-release-scl-rh
    $ yum -y install python27

    //Software Collectionsはインストールしただけでは利用できない．実際に利用するには以下のコマンドを実行する必要がある．
    $ scl enable python27 bash
    
    //常に使える状態にするためには~/.bashrcに追記
    source /opt/rh/python27/enable

pip7.1.0(python2.7以上はpip8.1.2は自動でインストールされる)

    $ yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-6.noarch.rpm
    $ yum -y install python-pip 
    
pyinotify 0.9.6

    $ pip install pyinotify

GitPython 2.1.10

    $ pip install gitpython

lsyncd

    $ yum -y install lsyncd

rsync

    $ yum -y isntall rsync  

Apache

    $ yum -y install httpd

Tomcat

    $ yum -y install tomcat



## バージョン確認コマンド一覧

CentOS  

    $ cat /etc/redhat-release  

Python

    $ python -V  

pip

    $ pip -V  

lsyncd

    $ lsyncd --version  

rsync

    $ rsync --version  

cron

    $ whereis -b crontab | cut -d' ' -f2 | xargs rpm -qf  

inotify

    $   

Apache

    $ httpd -v

Tomcat

    $ tomcat version


# Git

### gitコマンド
### よく使うコマンド
Initialize commit

    $ git init
    $ git add .
    $ git commit -m "コメント"

Clone command

    $ git clone git@


Add commit

    $ git add .
    $ git commit -m "コメント"

Delete commit

    $ git rm $(git ls-files --deleted)
    $ git commit -m "コメント"

Show log

    $ git log

Status git

    $ git status

Diff git

    $ git diff



# rsync




# lsyncd
### インストール方法

    $ yum -y install lsyncd

### 設定ファイルの編集

    $ cp -p /usr/share/doc/lsyncd-2.1.4/examples/lrsync.lua /etc/lsyncd.conf
    $ vi /etc/lsyncd.conf
    $ vi /etc/rsyncd.conf

### lsyncdのデーモン登録

    $ chkconfig --add lsyncd


# python
### インストール方法

    $ yum -y install python

pythonのバージョン確認コマンド

    $ python -V

上記コマンドを実行して，pythonのバージョンが表示されたらインストール完了．

# pip
### インストール方法

pyinotifyをインストールするためには，pipが必要になる．  
しかし，大学の環境ではpipはインストールされていない．  
そこで，pipをインストールする

一番簡単な方法

    $ 