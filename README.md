# run-for-Rec-main
这是一个关于如何运行Rec-main的项目

##程序运行（预处理）：

在Autodl上选择GPU，设置基础镜像
Pytorch-2.5.1
Python-3.12
Cuda-12.4

在Autodl中上传程序包以及数据集。
在Jupyterlab中进行相关操作
在根目录下创建文件夹（target_dir），将程序包解压至该文件夹下。
在sparkstep文件夹下，创建文件夹（0data），将数据集中的数据（202code2_query_bj文件夹）解压至此文件夹。
（先解压程序包以及数据集，然后创建对应的文件夹，再将对应的文件夹复制也可）
运行jupyter Notebook（run1_6）即可完成预处理工作。

如需运行其他城市数据集或bj城市完整数据集：
需对run1-6.ipynb的一些代码进行修改：

在第三个单元格后 修改日期以及城市简称
修改每个1-6py代码前的模拟命令行参数（按照数据集简称以及起始、结束日期，）（对于每个复制的1-6.py都要进行修改）
修改每个1-6py代码：测试集天数（test_day）（根据你想多少天数据作为测试集，需要小于数据集天数，不然训练集为空集）

##程序运行（Beijing、shanghai、shengzhen）
虚拟环境中安装要用到的包

安装torch-sparse
pip install torch-sparse -f https://data.pyg.org/whl/torch-2.5.1+cu124.html

安装torch-scatter
pip install torch-scatter -f https://data.pyg.org/whl/torch-2.5.1+cu124.html

pip install scikit-learn
