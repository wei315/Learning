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
  
