如何使用git？

   首先在本机生成ssh key以方便提交项目文件时不需要每次都输入用户名和密码
  
      如何生成？

      $ ssh-keygen -t rsa -C "xxxxxx@yy.com" //输入注册github时的邮箱地址
      $ 生成后会提示保存在哪个目录下 /xxx/id_rsa.pub
      $ cat /xxx/id_rsa.pub  //这里一定要使用cat不能使用vi 复制时会带回车符
      $ 将复制的key信息，粘贴到github.com里面,setting/ssh key下
  
  $ git --help

  1.复制一个项目到本地仓库？
      $ git clone [ssh address]

  2.提交一个修改?
      $ git add example.txt
      $ git status //查看状态
      $ 写remark
      $ git commit //提交
      $ git push //同步刷新
  3.如何恢复一个误删了的本地文件？
      $ git checkout example.txt //如果不起作用，先执行以下命令
      $ git reset --hard HEAD  //将提交重置
