# Nginx 入门

1. 在阿里云官网购买并启动一台云服务器，我选择的是centos系统。

2. 下载一款ssh工具连接云服务器。我这里用的是putty，windos下可免费安装。打开putty进行连接，输入购买时设置的账号密码，成功连接到云服务器。

3. 安装nginx环境
```
    yum -y install gcc gcc-c++ autoconf pcre pcre-devel make automake openssl openssl-devel
    
    yum -y install wget httpd-tools vim
```

4. 添加配置文件
```
    vi /etc/yum.repos.d/nginx.repo
```

修改配置文件内容为
```
    [nginx]
    name=nginx repo
    baseurl=http://nginx.org/packages/centos/7/$basearch/
    gpgcheck=0
    enabled=1
```
5. 安装nginx
```
    yum install nginx -y
```

6. 输入命令
```
    cd /etc/nginx/conf.d/
    
    vi default.conf             //查看配置文件

    cp default.conf ../         //拷贝文件到上层目录

    cd conf.d/

    vi default.conf             //修改配置文件
```

7. 下载node


# nginx 一些基本命令
```
    rpm -ql nginx 查询当前nginx的安装路径

    nginx -v 显示编译参数

    nginx -s reload   重新加载nginx

    systemctl start nginx 启动nginx

    systemctl stop nginx 停止nginx

    ps -ef | grep nginx 搜索关于nginx的进程

    cd etc/nginx && cat nginx.conf 查看nginx配置文件

    rm -rf .default.conf.swp 删除未保存的历史文件
```
