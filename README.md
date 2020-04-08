# vps-
本文为个人在日常使用中遇见的一些问题以及解决方案汇总  
仅供个人测试使用，切勿传播！！！  
1、服务器到手的环境以及文件配置： 
   更新软件包源并且安装curl  
apt-get update -y && apt-get install curl -y    ##Ubuntu/Debian 系统安装 Curl 方法  
yum update -y && yum install curl -y            ##Centos 系统安装 Curl 方法  
2、测速脚本（这里放两个比较常用的）  
    bash <(curl -Lso- https://git.io/superspeed)   ##国内三网测速，来体现你的主机在建站时的访问速度和延迟。  
    wget -qO- bench.sh | bash                      ##服务器的性能测试，IO和处理器等性能参数。  
       
3、wget "https://github.com/chiakge/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh ##安装bbr加速。  
4、v2ray 233一键脚本 bash <(curl -s -L https://git.io/v2ray.sh)   
5、安装宝塔面板更好的管理你的服务器  以下为官方安装教程：  
    找安装前需要打开你的服务器端口，具体发方法google你的服务器提供商+如何打开端口  
       centos安装命令：   
        yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh  
       Ubuntu/Deepin安装命令：  
        wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh && sudo bash install.sh  
       Debian安装命令：  
        wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh && bash install.sh  
       面板升级命令：  
        curl http://download.bt.cn/install/update6.sh|bash  
        安装后进入提示的网站登陆后选择安装mysql nignx php等环境  
  6、宝塔面板搭建wordpress博客  
      新建一个站点,php版本＞7.0，建好后进入网站根目录，删除index.html，然后远程下载一个wordpress的压缩包，也可自己下载后上传到服务器网站根目录将下载的文件解压到根目录即可访问到我们的wordpress安装界面。但是我们还需要配置我们的mysql数据库。我们选择数据库，新建一个数据库，记住你设置的参数。然后进入wordpress的安装环境。之后即可完成安装，这样你的博客就搭建完成了。  
