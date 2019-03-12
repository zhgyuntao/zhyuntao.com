---
title: "Vundle 安装与配置"
date: 2019-03-12T21:32:11+08:00
# draft: false
---

## 一、安装方式

### 1. 下载
```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

### 2. 配置
编辑 ``~/.vimrc``文件
```
set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'

" The following are examples of different formats supported.
" Keep Plugin commands between vundle#begin/end.
" plugin on GitHub repo
Plugin 'tpope/vim-fugitive'
" plugin from http://vim-scripts.org/vim/scripts.html
" Plugin 'L9'
" Git plugin not hosted on GitHub
Plugin 'git://git.wincent.com/command-t.git'
" git repos on your local machine (i.e. when working on your own plugin)
" Plugin 'file:///home/gmarik/path/to/plugin'         " 注释掉
" The sparkup vim script is in a subdirectory of this repo called vim.
" Pass the path to set the runtimepath properly.
Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
" Install L9 and avoid a Naming conflict if you've already installed a
" different version somewhere else.
" Plugin 'ascenator/L9', {'name': 'newL9'}

" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line
```

### 3. 安装
有两种方式安装插件
1. 进入vim
```
:PluginInstall
```

2. 命令行直接安装
```
vim +PluginInstall +qall
```

### 4. 其他命令
```
:bdelete    # 安装完成之后清除缓存
:PluginList     # 列出已安装的插件
:PluginClean    # 移除不在vimrc中配置，但是存在于vundle目录中的插件
:PluginUpdate   # 更新插件
```

## 二、配置

### 1. 其他插件推荐

1. YouCompleteMe    补全插件  
安装较为繁琐
2. NERDTree         目录树  
未完待续   
\TODO

---

> 参考地址  
> GitHub [VuldleVim/Vundle.vim](https://github.com/VundleVim/Vundle.vim)
