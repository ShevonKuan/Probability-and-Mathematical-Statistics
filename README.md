# <font color=orange>概率论</font> <font color=grey>课本</font> <font color=#0099ff>重要知识点整理与解读</font>
#### Shevon Kuan
## 简介

这是我基于 Latex2$\varepsilon$ 的数学笔记,它是一个系列并将使用一致的模板(目前仅部分开源),将来我可能会对该模板作独立开源处理.

**Demo:**
![element](https://github.com/ShevonKuan/Probability-and-Mathematical-Statistics/raw/master/readme_image/main.png)


----

## 编译介绍
```Latex``` 编译链```XeLaTex -> bibtex -> makeindex -> texindy -> xeLaTex重复编译```对应```VS Code```设置如下:
```json
"latex-workshop.latex.recipes": [
    {
        "name": "完整编译链",
        "tools": [
            "xelatex",
            "bibtex",
            "makeindex",
            "texindy",
            "xelatex",
            "xelatex"
        ]
    },
]
```
各命令具体配置如下：
```json
"latex-workshop.latex.tools": [
    {
        // 编译工具和命令
        "name": "xelatex",
        "command": "xelatex",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "%DOCFILE%"
        ]
    },
    {
        "name": "bibtex",
        "command": "bibtex",
        "args": [
            "%DOCFILE%"
        ]
    },
    {
        "name": "texindy",
        "command": "texindy",
        "args": [
            "%DOCFILE%.idx"
        ]
    },
    {
        "name": "makeindex",
        "command": "makeindex",
        "args": [
            "%DOCFILE%.nlo",
            "-s",
            "nomencl.ist",
            "-o",
            "%DOCFILE%.nls"
        ]
    }
],
```
----
## TODO:
列出该todo的目的是为了让我能够及时更新代码呐,不要天天顾着打游戏看视频.
- 6/22 - 6/28 完成第二章和第三章
- 优化图片储存架构
- 划分主文档
**目前进度 7%:**<font size=1 color=Lightgrey><font size=2 color=green>
- 第一章 概率论的基本概念
1 随机试验
2 样本空间、随机事件
3 频率与概率
4 等可能概型（古典概型）
5 条件概率
6 独立性<font size=3 color=orange> ⇦ 写到这里呐</font>
</font>
- 第二章 随机变量及其分布
1 随机变量
2 离散型随机变量及其分布律
3 随机变量的分布函数
4 连续型随机变量及其概率密度
5 随机变量的函数的分布

- 第三章 多维随机变量及其分布
1 二维随机变量
2 边缘分布
3 条件分布
4 相互独立的随机变量
5 两个随机变量的函数的分布

- 第四章 随机变量的数字特征
1 数学期望
2 方差
3 协方差及相关系数
4 矩、协方差矩阵

- 第五章 大数定律及中心极限定理
1 大数定律
2 中心极限定理

- 第六章 样本及抽样分布
1 随机样本
2 直方图和箱线图
3 抽样分布

- 第七章 参数估计
1 点估计
2 基于截尾样本的最大似然估计
3 估计量的评选标准
4 区间估计
5 正态总体均值与方差的区间估计
6 （0-1）分布参数的区间估计
7 单侧置信区间

- 第八章 假设检验
1 假设检验
2 正态总体均值的假设检验
3 正态总体方差的假设检验
4 置信区间与假设检验之间的关系
5 样本容量的选取
6 分布拟合检验
7 秩和检验
8 假设检验问题的p值法

- 第九章 方差分析及回归分析
1 单因素试验的方差分析
2 双因素试验的方差分析
3 一元线性回归
4 多元线性回归

- 第十章 bootstrap方法
1 非参数bootstrap方法
2 参数bootstrap方法

- 第十一章 在数理统计中应用Excel软件
1 概述
2 箱线图
3 假设检验
4 方差分析
5 一元线性回归
6 bootstrap方法、宏、VBA

- 第十二章 随机过程及其统计描述
1 随机过程的概念
2 随机过程的统计描述
3 泊松过程及维纳过程

- 第十三章 马尔可夫链
1 马尔可夫过程及其概率分布
2 多步转移概率的确定
3 遍历性

- 第十四章 平稳随机过程
1 平稳随机过程的概念
2 各态历经性
3 相关函数的性质
4 平稳随机过程的功率谱密度
</font>
## Contributors:

