---
title: 常用Markdown 语法  #在此处添加你的标题。
date: 2016-12-06
time: 21:15:02   #在此处输入你编辑这篇文章的时间。
categories: Exercise   #在此处输入这篇文章的分类。
toc: true  #在此处设定是否开启目录，需要主题支持。
tag: Markdown

---

[TOC]

</p>

Markdown 语法
===

## 各级标题

`# 一级标题`
`## 二级标题`
__...__
`###### 六级标题`

## 正文如下

__`这里是正文`__
这里是正文

## 引用（> 可实现引用效果，如下）

> This is a blockquote.
>
> This is the second paragraph in the blockquote.

## 4个空格 或 一个 tab （效果如下）

    With multiple paragraphs.

## 空行（网页换行符 /p）

` </p> `
</p>
## 链接
 `This is an [example link](http://example.com/ "With a Title").`
This is an [example link](http://example.com/"With a Title").

## 图片

`![alt text](/avatar/kumamon.png"七七")`
![alt text](/avatar/kumamon.png "七七")

## code (``)

> I strongly recommend against using any `<blink>` tags.
> I wish SmartyPants used named entities like `&mdash;`
> instead of decimal-encoded entites like `&#8212;`.

## 段落格式

### 字体
`*斜体文本*`  *斜体文本*

`_斜体文本_`  _斜体文本_

`**粗体文本**` **粗体文本**

`__粗体文本__`  __粗体文本__

`***粗斜体文本***`  ***粗斜体文本***

`___粗斜体文本___`  ___粗斜体文本___

***

### 分隔线
> 一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线

`***`

`* * *`

`*****`

`- - -`

`----------`

***

### 删除线
> 两个波浪线 ~~

`~~示例~~`  ~~示例~~

***

### 下划线
> 下划线可以通过 HTML 的 `<u>` 标签来实现：

`<u>带下划线文本</u>` <u>带下划线文本</u>

***


### 脚注
> 脚注是对文本的补充说明 中文可能无法正常显示

`[^要注明的文本]`  [^要注明的文本]


以下实例演示了脚注的用法：

创建脚注格式类似这样 [^RUNOOB]

[^RUNOOB]: description

***
***

## Markdown 列表
> Markdown 支持有序列表和无序列表。
无序列表使用星号(*)、加号(+)或是减号(-)作为列表标记：

* 第一项  `* 第一项`
* 第二项  `* 第二项`
* 第三项  `* 第三项`

+ 第一项  `+ 第一项`
+ 第二项  `+ 第二项`
+ 第三项  `+ 第三项`


- 第一项  `- 第一项`
- 第二项  `- 第二项`
- 第三项  `- 第三项`

> 有序列表使用数字并加上 . 号来表示，如

1. 第一项  `1. 第一项`
2. 第二项  `2. 第二项`
3. 第三项  `3. 第三项`

***
***

## Markdown 区块
> Markdown 区块引用是在段落开头使用 > 符号 ，然后后面紧跟一个空格符号

```
> 引用示例
> > 引用嵌套
```
> 引用示例
>
> > 引用嵌套

***
***

## Markdown 表格
> Markdown 制作表格使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行

语法格式如下
```
|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |
```

|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |

设置表格的对齐方式 
实例如下
```
-: 设置内容和标题栏居右对齐。
:- 设置内容和标题栏居左对齐。
:-: 设置内容和标题栏居中对齐。
```

| 左对齐 | 右对齐 | 居中对齐 |
| :-----| ----: | :----: |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |

***
***

## Markdown 高级技巧
> 支持的 HTML 元素
不在 Markdown 涵盖范围之内的标签，都可以直接在文档里面用 HTML 撰写
目前支持的 HTML 元素有：`<kbd> <b> <i> <em> <sup> <sub> <br>`等

示例

使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑

### 流程图
```
graph TD 从上到下
graph LR 从左到右
基本图形
id + [文字描述]矩形
id + (文字描述)圆角矩形
id + >文字描述]不对称的矩形
id + {文字描述}菱形
id + ((文字描述))圆形
```
```mermaid
graph LR
    start[开始] --> input[输入A,B,C]
    input --> conditionA{A是否大于B}
    conditionA -- YES --> conditionC{A是否大于C}
    conditionA -- NO --> conditionB{B是否大于C}
    conditionC -- YES --> printA[输出A]
    conditionC -- NO --> printC[输出C]
    conditionB -- YES --> printB[输出B]
    conditionB -- NO --> printC[输出C]
    printA --> stop[结束]
    printC --> stop
    printB --> stop
```

```mermaid
graph LR
    A[A] --> B[B] 
    A1[A] --- B1[B] 
    A4[A] -.- B4[B] 
    A5[A] -.-> B5[B] 
    A7[A] ==> B7[B] 
    A2[A] -- 描述 --- B2[B] 
    A3[A] -- 描述 --> B3[B] 
    A6[A] -. 描述 .-> B6[B] 
    A8[A] == 描述 ==> B8[B] 
```

```mermaid
graph TD
    root[bisp-root] -- 依赖 --> branch[bisp-common-branch]
    root[bisp-root] -- 依赖 --> center[bisp-common-center]
    root[bisp-root] -- 依赖 --> public[bisp-common-public]
    center -- 依赖 --> app[bisp-manage-front-app]
    app -- 依赖 --> backend[bisp-manage-backend]
    app -- 依赖 --> websource[bisp-manage-websource]
    backend -- 依赖 --> core[bisp-common-core]

    branch -- 依赖 --> core
    center -- 依赖 --> core
    public -- 依赖 --> core

    core -- 依赖 --> dependencies[bisp-dependencies]

    dependencies -- 依赖 --> ta3[bisp-dependencies-ta3]
    dependencies -- 依赖 --> thirdparty[bisp-dependencies-thirdparty]
```