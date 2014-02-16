fonttool里包括两个程序:
1. atlastool: 用来制作ZIM字体文件
2. zimtool: 把png转成zim文件
具体使用方法参看tools目录下的README.txt。

如何Build和更新fonttools:
A. Build方法(VS2013)
用VS2013打开tools\fonttool下的fonttool.sln项目文件编译。
PS: 在该目录下需要先创建libs目录，并放入事先编译好的libs文件(具体参见B.2, B.3 和 B.4)。

B. 更新fonttools源
1. tools里的atlastool.cpp和zimtool.cpp是源码，可以编辑更新。

2. 编译freetype
builds/win32/ 目录下选合适的vc工程文件编译
输出lib文件在objs/win32/里

3. 在ppsspp里编译native.lib和zlib.lib (_d的是调试版)。

4. 把三个lib文件freetype240.lib, native.lib(_d), zlib.lib(_d) 放在libs目录下。

5. 更新refs目录下的所有文件，都是PPSSPP里的文件夹，具体位置参见相关文件夹的说明档。
