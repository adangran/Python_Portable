Created Time: 2020.09.24 星期四 19:23:36

## Python 绿色版本的制作

### 下载python release版本

下载地址：https://www.python.org/ftp/python/

下载最新版本，如https://www.python.org/ftp/python/3.8.6/ 目录下的 python-3.8.6rc1-embed-win32.zip  

解压到 %USERPROFILE%\AppData\Local\Python\

### 安装pip

下载地址：https://pip.pypa.io/en/stable/installing/

如果是cmder，可进运行命令：

```shell
curl https://bootstrap.pypa.io/get-pip.py -o %USERPROFILE%\AppData\Local\Python\get-pip.py
```

安装命令：

```shell
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\get-pip.py
```

安装完成后，文件夹中会增加Lib和Scripts两个文件夹

### 修改python38._pth文件(38根据python版本的不同会不同)

记事本打开python38._pth，去除import site的注释，最终修改如下：

```shell
python38.zip
.
 
# Uncomment to run site.main() automatically
import site
```

### 安装lib

#### 查看已安装lib

运行cmder（或cmd），进入到%USERPROFILE%\Local\Python\ ，运行 .\python.exe .\Scripts\pip.exe list， 结果如下：

```shell
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\Scripts\pip.exe
Package    Version
---------- -------
pip        20.2.3
setuptools 50.3.0
wheel      0.35.1
```

#### 安装新lib

以安装vim需要用到的库为例，输入以下命令：

```shell
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\Scripts\pip.exe install pylint
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\Scripts\pip.exe install flake8
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\Scripts\pip.exe install autopep8
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\Scripts\pip.exe install rstcheck
%USERPROFILE%\AppData\Local\Python\python.exe %USERPROFILE%\AppData\Local\Python\Scripts\pip.exe install jedi
```

### 运行python

```shell
%USERPROFILE%\AppData\Local\Python\python.exe
```