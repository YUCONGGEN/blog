---
title: 开始机器学习之前：配置开发环境
author: 郁
coverImg: /medias/banner/8.jpg
top: false
cover: true
toc: true
mathjax: false
summary: >-
  Jupyter lab是Jupyter
  Notebook的升级版，页面更加美观操作更加简便，和Notebook一样是anaconda自带，在cmd或者anaconda
  prompt里面输入Jupyter lab即可打开，或者也可以在Anaconda页面中找到它的接口。 
tags:
  - 机器学习
  - 配置开发环境
categories:
  - 机器学习篇
reprintPolicy: cc_by
abbrlink: d2d6104d
date: 2020-09-04 00:00:00
img:
password:
---

# **开始机器学习之前：配置开发环境**

## 开发环境：Jupyter-notebook

课程中的开发环境是**Jupyter lab**，Jupyter lab是Jupyter Notebook的升级版，页面更加美观操作更加简便，和Notebook一样是anaconda自带，在cmd或者anaconda prompt里面输入Jupyter lab即可打开，或者也可以在Anaconda页面中找到它的接口。Jupyter lab中大部分操作都和Notebook一样，每个人电脑的设置不同，可能存在Jupyter lab无法使用的情况。

![ ](http://qyxthf420.hn-bkt.clouddn.com/1-1.png)

## 所需库和版本（基于anaconda)

课程中需要使用到的库/模块，以及我所使用的版本供大家参考：**Anaconda**：4.6.8（你的版本最少要4.6.7或以上) **Python** 3.7.2 （你的版本至少要3.6或以上) **Scikit-learn** 0.20.3 （你的版本至少要0.20或以上) **Graphviz** 0.8.4  **NumPy** 1.16.2  **Pandas** 0.24.2（你的版本至少要0.23或以上)  **Matplotlib** 3.0.3   **SciPy** 1.2.1

以上的库和模块都是必须的，版本可以不用太过限制不过尽量保持和需求的一致会比较理想。这些库大部分是anaconda自带的，但是graphviz需要自行安装，详情请参考“安装graphviz”章节。你可以使用以下代码来查看你现在所安装的版本和库是否达到要求，如果没有达到要求，请参考下面的部分来进行更新/安装：

#导入所需要的库

```python
#导入所需要的库
import pandas as pd
import numpy as np
import sklearn
import matplotlib as mlp
import scipy
```

如果出现"no module named xxxx"这样的错误，证明你的计算机缺乏xxxx库，则需要另行安装。另行安装的时候，

请在cmd或者anaconda prompt里面运行以下代码。**缺哪个库，安哪个库，切勿覆盖/重新安装已存在的库**。注意，安装时一次一行，一次一库。

```python
#在cmd或anaconda prompt中逐行运行
conda install numpy
conda install pandas
conda install scipy
conda install matplotlib
conda install scikit-learn
```

如果导入没有报错，你可以继续运行下面的代码来查看你的anaconda版本：

```python
conda -v
```

并运行以下代码来查看你的Python版本：

```python
Python -v
```

你可使用以下代码来查看你其他库的版本：

```python
module = [pd,np,sklearn,mlp,scipy]
name = ["pandas","numpy","sklearn","matplotlib","scipy"]
for name,item in zip(name,module):
		print("{}:{}".format(name,item.__version__))
```

如果你的Python版本或任意库的版本不足，可以使用以下代码对各个模块和库进行更新。

```python
#在cmd或anaconda prompt中逐行运行
#更新anaconda(可能耗时较长时间)
conda update -n base -c defaults conda
#更新Python
conda update python
#更新所需要的库
conda update pandas
conda update numpy
conda update scipy
conda update matplotlib
conda update scikit-learn
#一次性更新anaconda下面所有的库(可能耗时较长时间)
conda update --all
```

在许多时候，我们也通过pip进行操作，但如果能够使用Anaconda，就不推荐使用pip。pip安装一部分库的时候可能会出现异常，原因是pip默认下载的一部分库的版本（如SciPy）可能只适用于linux系统，而Anaconda的安装一般不会有这个问题。对于能够自己排查出现的问题的学员，请随意选择任何安装方式。但注意，Anaconda的安装和pip的安装尽量不要混用，由Anaconda安装的库在使用pip卸载或是更新的时候，可能出现无法卸载干净，无法正常更新，或更新后一部分库变得无法运行的情况。安装过程中任何的报错，都可以通过卸载重装来解决问题，这是最有效的方式。

## 安装和配置**graphviz**

graphviz是我们算法模块中比较重要的一个库，我们会使用它来对我们的重要算法：决策树进行绘图。通常来说graphviz都不太可能是自带的。Mac系统下安装graphviz相对简单，可以参考博文：https://blog.csdn.net/qq_36847641/article/details/78224910。


