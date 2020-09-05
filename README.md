# APUE学习笔记

我是在mac上开发的，所以第一步大概就是解决下跑代码的环境问题，因为Mac本身就是UNIX系的，所以跑APUE的代码也算是有着天然的优势吧~

- 书的网址：http://www.apuebook.com/apue3e.html
- 下载地址：http://www.apuebook.com/src.3e.tar.gz

下载好之后就是解压：

```
tar -zxvf src.3e.tar.gz -C ~/CLionProjects/APUE-study-code/
cd ~/CLionProjects/APUE-study-code/apue.3e
```

然后，将error.c和apue.h拷贝到系统的相应路径：

```
cp include/apue.h /usr/local/include
cp lib/error.c /usr/local/include/
```

接下来，将error.c include进apue.h：

```
vim /usr/local/include/apue.h
```

在最后一行 `#endif` 前加上一行：`#include "error.c"`，搞定~

最后，回到apue.3e目录，然后运行 `make`，没有报错就说明成功了哈~
