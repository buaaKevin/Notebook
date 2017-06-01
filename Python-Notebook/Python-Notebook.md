
logging模块
----

### 日志级别：

CRITICAL > ERROR > WARNING > INFO > DEBUG > NOTSET

| **级别**	| **何时使用** | 
| :----: | :----: |
| DEBUG	| 详细信息，典型地调试问题时会感兴趣。|
| INFO	| 证明事情按预期工作。|
| WARNING	| 表明发生了一些意外，或者不久的将来会发生问题（如‘磁盘满了’）。软件还是在正常工作。|
|　ERROR	| 由于更严重的问题，软件已不能执行一些功能了。|
|　CRITICAL |	严重错误，表明软件已不能继续运行了。|


### 可自定义日志级别：


    import logging

    logging.basicConfig(
                        level=logging.WARNING,
                        format='%(asctime)s %(levelname)s %(message)s',
                        filename='myapp.log',
                        filemode='w')

    logging.debug('Debug message')
    logging.info('Info message')
    logging.warning('Warning message')


**logging.basicConfig 函数** 各参数:

> filename: 指定日志文件名
>
> filemode: 和file函数意义相同，指定日志文件的打开模式，'w'或'a'
>
> format: 指定输出的格式和内容，format可以输出很多有用信息，如上例所示:
>
>  - %(levelno)s: 打印日志级别的数值
>  - %(levelname)s: 打印日志级别名称
>  - %(pathname)s: 打印当前执行程序的路径，其实就是sys.argv[0]
>  - %(filename)s: 打印当前执行程序名
>  - %(funcName)s: 打印日志的当前函数
>  - %(lineno)d: 打印日志的当前行号
>  - %(asctime)s: 打印日志的时间
>  - %(thread)d: 打印线程ID
>  - %(threadName)s: 打印线程名称
>  - %(process)d: 打印进程ID
>  - %(message)s: 打印日志信息
>
> datefmt: 指定时间格式，同time.strftime()
>
> level: 设置日志级别，默认为logging.WARNING
>
> stream: 指定将日志的输出流，可以指定输出到sys.stderr,sys.stdout或者文件，默认输出到sys.stderr，当stream和filename同时指定时，stream被忽略

[python 的日志logging模块学习](http://blog.csdn.net/yatere/article/details/6655445)

[python logging模块使用教程](http://www.jianshu.com/p/feb86c06c4f4)

[使用python的logging模块](http://kenby.iteye.com/blog/1162698)

---

---


requirements.txt
----

requirements.txt 文件 里面记录了当前程序的所有依赖包及其精确版本号。

这个文件有点类似与Rails的Gemfile。
其作用是用来在另一台PC上重新构建项目所需要的运行环境依赖。

生成requirements.txt文件

	pip freeze > requirements.txt

安装requirements.txt依赖

	pip install -r requirements.txt

---

---

__future__ 模块
----

[python的__future__模块](http://www.cnblogs.com/ksedz/p/3190208.html)：
	运用

	首先是可以做个性化的用法，比如你喜欢用print（）而不是print

	更重要的是基本用以下几句就可以让python2和python3有良好的兼容性了

	from __future__ import print_function
	from __future__ import unicode_literals
	from __future__ import division
	from __future__ import absolute_import
	
[Python future模块常见示例相关解读](http://developer.51cto.com/art/201003/186805.htm)：

	如果使用这个语句，则该语句必须是模块或程序的第一个语句。
	此外，'__ future__' 模块中存在的特性最终将成为Python语言标准的一部分。
	到那时，将不再需要使用Python future模块。

---

---

下载指定url文件到指定的本地目录
---

[代码模板](https://github.com/JNingWei/Python-Applet/blob/master/DownloadFileFromUrl/down.py)

---

---

os模块
---

api|annotation
---|---
os.listdir()|列出当前目录下的所有文件和文件夹
os.system()|运行shell命令(接收命令行列出当前目录下的所有文件和文件夹参数)
os.sep()|更改操作系统中的路径分隔符
os.path.isfile()|文件是否存在
os.path.isdir()|文件夹是否存在
os.path.exists()|路径是否存在
os.getcwd()|获取当前路径(中间会自动添上一个路径分隔符)
os.remove()|删除指定文件
os.rmdir()|删除空文件夹
os.mkdir()|新建文件夹
os.chdir()|改变当前目录到指定目录中

---

---

shutil模块
---

api|annotation
---|---
shutil.rmtree()|删除非空文件夹树

---

---

import模块
---

关于　**import scipy** 为什么不能导入　**scipy.misc.imsave** 模块：

[个人理解]()

---

---
