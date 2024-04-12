离线版cpu yolo8图形物体检测环境

```
# google search: python embeddable pip install
# 参考：https://stackoverflow.com/questions/42666121/pip-with-embedded-python
# 打开https://www.python.org/downloads/release/python-3123/，下载：Windows embeddable package (64-bit)
# 解压，修改python312._pth，里面有一行#import site把最前面的井号删掉，最下面一行添加：Lib\site-packages
# 打开https://pip.pypa.io/en/stable/installation/，下载get-pip.py
> set http_proxy=http://127.0.0.1:7890
> set https_proxy=http://127.0.0.1:7890
> python.exe get-pip.py
> python.exe -m pip install -r requirements.txt         // 推荐
> python.exe -m pip list                                // 推荐
> .\Scripts\pip install -r requirements.txt             // 不推荐
> .\Scripts\pip list                                    // 不推荐

测试，命令行运行python.exe test.py     文件内容如下：
import cv2
import torch
import ultralytics

print(cv2.__version__)
print(torch.__version__)
print(ultralytics.__version__)
print("Hello, World!")
```



