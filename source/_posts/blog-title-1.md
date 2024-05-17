---
title: 2024春季开源操作系统第一阶段学习记录
date: 2024-05-03 14:44:57
tags:
    - author:thekingyx
categories:
    - 2024春夏季开源操作系统训练营
---
### 开源rCore项目初识
- time：about 2023/8~10

  最初接触操作系统的经历十分巧合，因为是刚从土木老哥转到cau的cs大类，刚入行的紧迫感鞭策我不断搜集信息。恰好本系某位大佬前辈（人称炸药哥）钟爱操作系统，已经不只一次向我们强烈安利此项目，但去年由于考研以及学（da）业（bai）繁（te）忙（bai），虽然报了名，但完全没做.....
  
  今年又到了开营的时间，同时经过半年多的摸爬滚打，对于自己今后发展方向也有了大致的轮廓，也算是借着rust的强大能力，帮我去理解RISC-V的原理，为今后科研打下基础！
### 配置rust编译环境
- time：2024/4/11-2024/4/12

  心累的一晚上，由于第一次接触github，第一次安装wsl2，没有实际上手过跑在Linux环境下的项目，rustling的配置遇到了超级多的问题。习惯root权限进行Linux操作，这个坏习惯给我带来了巨大的困难，例如vscode无法访问wsl内文件，以及git无法提交代码至仓库......
  多次修改权限无果后，最后决定全盘重新装（前前后后弄了3-4个小时），还好最后终于配置好了环境，终于可以开始和rust斗智斗勇了。
### 基本变量和if类型（包括综合quiz练习）
- time：2024/4/13
  ##### 心得体会
  初见rust，接触前几道题并没有太大难度，经历基本的rust环境编译后，最初的几道题做起来真的舒心不少。quiz1练习提供了一个基本的语法综合训练。目前感觉rust并没有传说中那么大的难度qwq。
  ##### 收获
  了解了if的使用方法，和c语言最大的不同就是变量不可修改（修改必须要mut），所有权以及的命名使用规则，理解起来还是比较容易的。
### 基本数据类型和vec
- time：2024/4/16
  ##### 心得体会
   最近课太多了，鸽了几天。不知道是，手生了还是变难了，总感觉难度陡增，尤其是vecs2，网上搜了一下都没太搞懂（后买翻答疑发现是后面的课程，我：“？？？？”）
  ##### 收获
  发现基本数据类型和c还是有相似之处的，只是代码表达方式上要别扭很多，往往是，逻辑清楚，不知道怎么改。在vec的一系列题中，这种问题尤为明显。所有权类的题仔细思考后还是有思路的。
### 所有权
- time：2024/4/20
  ##### 心得体会+收获
  所有权类的题仔细思考后还是有思路的。最大的问题还是读代码的能力欠缺，面对“一大坨”代码无从下手，经历这一系列的作答，还是收获满满
### struct类型
- time：2024/4/20
  ##### 心得体会
  难度骤增，这种类c的结构体真的很容易出现小毛病，对于我这种基础不牢的人来说真的是拉到了新的难度等级，每道题要花一些时间去想emmm，又到了快凌晨一点，睡！！
  ##### 收获
  基本了解了struct的命名使用规则，深一脚浅一脚往下走叭
### 枚举类型，包，模块
- time：2024/4/25
  ##### 心得体会
  好吧，这周课程依旧很多,又拖了好久,新知识吸收速度好慢,今天的枚举总体来说类似struct，学习应用起来并不难。模块主要在封装层面用途很大，就是改变量名字很捉急......
  ##### 收获
  了解枚举定义，以及如何创建成员，熟悉如何在不同模块中修改名称以及引入不同的库.
### 哈希表创建，option枚举，error系列练习
- time：2024/4/26
  ##### 心得体会
  哈希表提供了一个可以快速管理数据的方法，但是读代码好痛苦，太不熟悉了。option同昨天的枚举相似，做起来熟练很多。error的习题考察的好综合，经常改着改着就把整个代码弄乱了......遂ctrl^z重新来过（捂脸）
  ##### 收获
  了解哈希表以及option枚举类型如何使用，加深了对如何处理不同错误的理解，并了解如何修改（或许）
### 泛型扩展，trait，生命周期，test练习，迭代器
- time：2024/4/27
  ##### 心得体会
  重新见到泛型，做的也得心应手起来了。越来越感觉在严谨的rust中，泛型真算一个万金油，又能保证封装，还能调用方便，赞。trait反而更像一个接口（就是我做的什么别人也可以借用的感觉）。
  生命周期emmm,某个元素需不需要活，活多久，怎么活......都是其他语言没有的"独特"含义。虽然理解起来费劲，但是题目比较简单。test练习又是两眼一抹黑的翻资料去做，练习需要的广度比课程上要求的多得多。
  迭代器给了一个遍历元素的方法，但是迭代器是惰性的，使用前需要先调用。
  ##### 收获
  扩充了在方法中使用泛型的实例，了解trait如何在不同函数或结构体中实现，浅显的理解生命周期含义，知道test函数基本语法，迭代器如何声明与调用
### 余下内容，Rc< T >，box等
- time：2024/4/28
  ##### 心得体会
  后面的语法更趋向于数据某种数据结构，理解起来很容易，但运用很难。好在题目并不难，有的题哪怕不了解此类语法也能通过联系上下文做出来（虽然对于提升并没有什么帮助），不过鉴于此项目本质为写os，rust的深度学习就留在需要的时候了（手动狗头）
  ##### 收获
  了解box，Rc，Arc，等结构体的使用环境，了解多线程如何创建，了解宏的创建和使用，接触代码分析工具Clippy。以及如何实现数据结构
