# Software

## Description
- The following is a list of my summarize. (enrolled, completed, interested)
- The order does not matter
- The list is created on my own experience.

### contant

- **GitHub**
  
  The document is the content of the GitHub

- **Tensorflow**

### 安装WINDOWS版本的Tensorflow 2.1.0(CPU & GPU)  
**准备**
- Anaconda3-2020.02-Windows-x86_64.exe [Download](https://www.anaconda.com/distribution/)
- cuda_10.1.168_425.25_win10.exe [Download](https://developer.nvidia.com/cuda-toolkit-archive)
- cudnn-10.1-windows10-x64-v7.6.4.38.zip [Download](https://developer.nvidia.com/rdp/cudnn-download)
- mkl-2019.0-py2.py3-none-win_amd64.whl [Download](https://pypi.org/project/mkl/#files)
- opencv_python-4.2.0.32-cp37-cp37m-win_amd64.whl [Download](https://pypi.org/search/?q=opencv)
- tensorflow-2.1.0-cp37-cp37m-win_amd64.whl [Download](https://pypi.org/search/?q=tensorflow&o=)
- VC_redist.x64 .exe [Download](https://www.microsoft.com/zh-cn/download/confirmation.aspx?id=52685)  
*注意*
- 这些文件的版本都是有要求的，版本过高或过低都有可能导致安装不成功
- 电脑里面有Visual Studio(需要C++部分)的话，可以省区很多麻烦事情，如果没有也可以下载相应的环境（缺少C++的环境，可能导致缺失.dll文件）
- 2.0以上版本的tensorflow是CPU和GPU集成在一块的  

**步骤**  
   1 安装Visual Studio，或者安装VC_redist.x64 .exe   
  本人由于电脑原因，Visual Studio占用过大，且不经常用，所以直接安装需要的环境即可     
   2 先安装Anaconda [网上有很多教程](https://blog.csdn.net/u012318074/article/details/77075209)  
  安装时候注意要勾选自动生成环境变量    
   3 打开cmd，然后可以查看，以及安装tensorflow    
 - pip list 查看安装的包  
 - pip install （pip install --upgrade numpy；  pip install --upgrade scipy；  pip install --upgrade pandas；
  pip install --upgrade keras；  pip install --upgrade matplotlib）  
 - 如果网速慢的话，可以网上查找一些镜像[清华，网易 ect.](https://blog.csdn.net/lambert310/article/details/52412059)   
 - 如果只用CPU的话，这里要查看一下mkl的包有没有，没有的话安装上   
   4 继续安装GPU版本[可以参考1](https://blog.csdn.net/WWTOR/article/details/80603296)[可以参考2](https://www.cnblogs.com/sorex/p/7615185.html)[可以参考3](https://zhuanlan.zhihu.com/p/107683614)  
  第一步：就是安装CUDA    
 - 在安装的过程中，可能会有安装失败的可能性， CUDA安装失败(参考)[https://blog.csdn.net/zzpong/article/details/80282814]  
 - 本人是直接选择自定义，然后全部安装    
 第二步：就是安装cuDNN   
 cuDNN下载之后解压后覆盖到C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1目录下即可   
   5 安装成功  
 - cmd输入python，然后import tensorflow检验
  

- **JDK（LINUX）**
  **准备**
- 如果包在本地，要上传到服务器上，可以通过ftp
- 解压压缩包，tar xzvf /srv/ftp/jdk -C /user/local/
- 解压缩之后得到JDK的保存目录，讲其更名：mv /user/local/jdk.1.9/ /user/local/jdk
- 在JDK的bin目录里面有所有的java可执行的命令，但需要配置到环境属性中
- 环境属性配置：JDK环境支持，将jdk的路径配置进去：
  ·打开配置文件 vim /etc/profile
  ·追加两个配置项：
  1、定义java_home环境的属性：export JAVA_HOME=/usr/local/jdk
  2、将java的执行文件配置到可执行的路径中命令,：export PATH=$PATH:$JAVA_HOME/bin:（：配置分割符）
- 使配置立即生效：source /etc/profile
- 如果可以执行java的命令，则代表配置成功：直接输入“java”  
*注意*
- env查看用户的配置环境
- ifconfig可以查看Ubuntu的ip地址
- :wq与:q!的区别


  - **Tomcat（LINUX）**
  **准备**
- Tomcat是web开发的一个重要容器，首先要安装JDK，然后在其环境下配置Tomcat（需要JAVA_Home）
- Tomcat软件包下载到指定目录下“/tomcat”:wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.38/bin/apache-tomcat-9.0.38.tar.gz（进入目录命令：cd /home/zw/tomcat）
- 解压缩处理：tar xzvf 文件名称.tar.gz -C /其他目录路径
- 解压缩文件更名： mv /文件夹 /文件夹
- 环境属性配置：JDK环境支持，将jdk的路径配置进去
  ·打开配置文件：vim /tomcat/bin/setclasspath.sh
  ·在setclasspath.sh文件的头部追加如下的环境内容定义：export JAVA_HOME=/uer/local/jdk、JRE_HOME==/uer/local/jdk/jre
- 默认的tomcat是工作在8080端口上的，现在可以修改为80端口
  ·打开配置文件：tomcat/conf/server.xml
  ·修改连接端口
- 配置完成后进行tomcat的
  ·启动：/tomcat/bin/catalina.sh start 
  ·停止：/tomcat/bin/catalina.sh start
- 查看所有端口：netstat -nptl
-tomcat本身是基于JDK运行的，所以如果想在系统中查看所有与java相关的进程的时候，可以输入“jps”查看（如果有booststrap则证明启动了），进入tomcat下面的logs，more 文件名称
-ifconfig查看ip地址，然后通过浏览器打开。
*注意*
- 首先要配置好JDK 命令：Java -version
- ununtu切换到home下，给自己用户授权，sudo chmod -R 777 zw，然后切换到自己的用户 su - zw


- **HTTPS（LINUX）**
  **准备**
- 1、为服务器生成证书（非信任的证书）：使用keytool为tomcat生成证书，这里面有个注意事项，在输入用户名的时候有两种方式（localhost/IP地址--浏览器输入的地址和证书的地址是否一致），其他的选项无所谓
keytool -genkey -v -alias tomcat -keyalg RSA -keystore /home/zw/tomcat/tomcat.keystore -validity 36500
- Tomcat软件包下载到指定目录下“/tomcat”:wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.38/bin/apache-tomcat-9.0.38.tar.gz（进入目录命令：cd /home/zw/tomcat）
- 2、为客户端生成证书（用户名输入localhost）
keytool -genkey -v -alias mykey -keyalg RSA -storetype PKCS12 -keystore /home/zw/tomcat/mykey.p12
- 3、让服务器信任客户端证书
keytool -export -alias mykey -keystore /home/zw/tomcat/mykey.p12 -storetype PKCS12 -storepass 123456 -rfc -file /home/zw/tomcat/mykey.cer
- 4、是将该文件导入到服务器的证书库，添加为一个信任证书使用命令如下：
keytool -import -v -file /home/zw/tomcat/mykey.cer -keystore /home/zw/tomcat/tomcat.keystore
- 5、让客户端信任服务器证书
keytool -keystore /home/zw/tomcat/tomcat.keystore -export -alias tomcat -file /home/zw/tomcat/tomcat.cer
- 6、配置tomcat文件：tomcat/conf/server.xml

<Connector port="8443" protocol="org.apache.coyote.http11.Http11NioProtocol"

 SSLEnabled="true" maxThreads="150" scheme="https"

 secure="ture" clientAuth="ture" sslProtocol="TLS"

 keystoreFile="/home/zw/tomcat/tomcat.keystore" keystorePass="123456"

 truststoreFile="/home/zw/tomcat/tomcat.keystore" truststorePass="123456"     />

其他说明：
keystoreFile：服务器证书文件路径
keystorePass：服务器证书密码
truststoreFile：用来验证客户端证书的根证书，这就是服务器证书
truststorePass：证书服务器密码
- 7、测试：
  ·启动tomcat：位置到tomcat/bin目录下./startup.sh
  ·停止tomcat：./shutdown.sh
  ·查看：tail -f ../logs/catalina.out(查看tomcat是否启动)
  ·访问：https://localhost:8443（localhost:8080看一下是否可以进入tomcat的管理页面）
  ·检查证书用户名是不是设置的是localhost
  ·在浏览器中--设置--安全--证书管理--添加证书（mykey.p12）添加证书
*注意*
- 首先输入java看一下环境是否正确
- ununtu切换到home下，给自己用户授权，sudo chmod -R 777 zw，然后切换到自己的用户 su - zw

