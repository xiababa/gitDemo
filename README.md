# gitDemo
git demo第一个案例

github是啥? 它是git的一个远程服务器.
git是啥? 是一个分布式代码管理工具.

连接github步骤?
  1.首先要先创建一个github的账号
  2.在github上创建一个仓库(改成ssh协议)
  3.在另一个装有git的主机上生成一个密钥
     3.1 命令:ssh-keygen -t rsa 存放位置C:\Users\用户名\.ssh\
     3.2 在github个人信息setting中添加一个ssh key,title随便起,key就是生成的pub 公共密钥
  4.在主机上执行git remote add origin git@github.com:github用户名/仓库名.git 创建一个用户
     4.1 如果已经存在可以先删除,命令: $ git remote rm origin
  5.将主机本地仓库的代码同步到github的远程仓库上
     5.1 使用命令方式:git push -u origin master
     5.2 使用git小乌龟方式需要先设置ssh的架构
        5.2.1:右键本地仓库
        5.2.2:点击小乌龟在找到setting
        5.2.3:网络选项配置ssh客户端:C:\Program Files\Git\usr\bin\ssh.exe
        5.2.4:git选项远端选项配置拦截github的连接信息:url和推送都设置成 git@github.com:github用户名/仓库名.git
        5.2.5 配置完成后右键本地仓库点击小乌龟选择推送,推送到配置的连接信息即可
        
在github上部署项目
  进入仓库,点击setting找到page set将none改成仓库master.并保存.然后再找到page set边框外会显示此仓库的网址


