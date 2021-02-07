---
title: Fish Shell
top: false
cover: false
toc: true
mathjax: true
date: 2021-02-05 15:46:20
password:
summary:
tags:
  - liunx
categories:
  - Markdown
---
### Fish Shell - 比 zsh 更简洁实用的 Shell

```plain
一直没有兴趣折腾 zsh，安装了 
oh-my-zsh
 也是无奈之举，配置起来异常繁琐，关键还很不流畅。最近想添加个文件子目录自动补齐的功能，愣是没配置成功。所以，我果断尝试了一下 fish shell。
```

  

### fish shell 吸引我的地方

1.  完全不需要配置，开箱即用（Works Out Of The Box，学了个新词）。省去了 zsh 和 oh-my-zsh 的配置麻烦。
    
2.  基于 history 自动提示
    
3.  可以自动补齐路径，例如，路径中使用 \*\* 自动补全子目录
    
4.  语法更人性化一些。例如，for 循环等，比 bash 的反人类语法好很多。
    
5.  文档写的挺有意思
    

ubuntu 18.04 上安装 fish shell

```ps
sudo apt-add-repository ppa:fish-shell/release-2
sudo apt-get update
sudo apt-get install fish
启动 fish shell
$ fish
```

  

#### 我才明白为何 shell 脚本第一行要加

#!/bin/bash

```plain
因为不同 shell 的语法不同，所以需要指明 shell 类型。
例如 fish shell 与 bash shell 的 for 循环语法就不一致。
但是，这并不妨碍我们在 fish shell 中执行 bash shell 语法写的脚本。
```

  

#### 设置 tmux 默认使用 fish shell

```plain
~/.tmux.conf
set -g default-shell /usr/bin/fish 
set -g default-command /usr/bin/fish 
fish_config 基于网页视图修改 fish shell 配置
非常有创意
$ fish_config
Web config started at 'file:///home/zhongwei/.cache/fish/web_config-GP7QKR.html'. Hit enter to stop.
```

  

参考

[https://fishshell.com/](https://fishshell.com/)

配合fish使用终极搜索神器fzf

~/.config/fish/functions/fish\_user\_key_bindings.fish

function fish\_user\_key\_bindings fzf\_key_bindings end
