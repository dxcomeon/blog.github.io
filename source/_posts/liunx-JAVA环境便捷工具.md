---

title: liunx_JAVA环境便捷工具
date: 2021-02-03 17:50:07
categories: Markdown
tags:

- liunx
- java

---

### 1.sdkman介绍  

```sh
  sdkman(The Software Development Kit Manager), 中文名为:软件开发工具管理器．这个工具的主要用途是用来解决在类unix
　操作系统(如mac, linux等)中多种版本开发工具的切换, 安装和卸载的工作．对于windows系统的用户可以使用Powershell CLI来体验．
　例如: 项目A使用Jdk7中某些特性在后续版本中被移除（尽管这是不好的设计），项目B使用Jdk8,
　我们在切换开发这两个项目的时候，需要不断的切换系统中的JAVA_PATH,这样很不方便，如果存在很多个类似的版本依赖问题，
　就会给工作带来很多不必要的麻烦． 
　　 
　sdkman这个工具就可以很好的解决这类问题，它的工作原理是自己维护多个版本，当用户需要指定版本时，
　sdkman会查询自己所管理的多版本软件中对应的版本号，并将它所在的路径设置到系统PATH.
```

### 2.安装

```sh
curl -s http://get.sdkman.io | bash
```

上面的命令的含义: 首先sdkman官网下载对应的安装shell script，然后调用bash解析器去执行．

接下来，你需要打开一个新的终端窗口，执行命令:

```sh
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

再次之后，可以通过输入sdk help确认安装是否完成.

### 3.使用

1\. 例子:安装jdk最新版本

```sh
 sdk install jdk
```

2\. 安装指定版本的软件

```sh
sdk install jdk 8
```

3.安装本地版本

```sh
 sdk install jdk-8 /path/to/jdk-8
```

4.删除执行版本

```sh
sdk remove scala 2.11.6
```

5.列举可供安装的软件列表

```sh
    sdk list
```

