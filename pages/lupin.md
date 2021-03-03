---
title: Lupin
---

## 参考资料
#### [Handuo同学的教程](https://cn.logseq.com/t/topic/314) 初看起来非常复杂，找到下面的原始出处看了一下。
#### [Lupin的Github代码库](https://github.com/akhater/Lupin) 实际看不懂，还是要靠Handuo。
## 电脑白痴问题一箩筐
### 问题1：知道自己有python，之前破解Digital Paper用过的，然而不会用pip命令，确切地说不知道装过没有。
#### 解决：去下载了最新的 [Python 3.9.2](https://www.python.org/downloads/release/python-392/)，据说自带pip。但是仍然不行，最后上网搜了一下，说是pip命令要在python环境外面而不是里面用，一激动进入python之后就找不到了，得在cmd下面用。然后会用了之后说pip要更新，但是好在连命令都在提示了给出来了，更新之后没啥可见的变化。
### 问题2：第二大命令git没有……
#### 解决：这次学乖了，先去搜了一下git是什么，找到一个 [git安装包](https://git-scm.com/download/win) ，装上试了一下。有一个叫做Git GUI的东西，可以clone，设置源和目的地都非常容易。然后还有一个叫做Git Bash的，打开像是个terminal，这里可以用`git pull origin master`命令，用于更新。
### 问题3：main.py无法运行
#### 解决：首先从C盘无法cd拖拽文件夹直接进入，网上搜了一下需要先打d:进入D盘才行。然后`python main.py`一句运行了好久好久，最后说连接失败。论坛上说是telegram api要命令行翻墙，然而不会，目前死在了这一步，按照网上说的换了各种端口都不行。不过logseq右侧栏现在已经出现了日历，这个已经好用。然后第二天发现当天的日志无法写入……但是其他的页面可以，怀疑遇到了Handuo说的时间问题，于是不解决不行啊。今天继续研究软件问题吧。
#### 实验了一下午加一早上，最后发现GitHub上一个 [不知讨论什么的页面](https://gist.github.com/dreamlu/cf7cbc0b8329ac145fa44342d6a1c01d#gistcomment-3441244) 提到不能用cmd，而是要用powershell，于是试了一下，成功~ powershell还可以直接进入文件夹不用单独换盘符。但是proxy是每次打开都要重新设一下。
### 问题4：telegram输入的内容在logseq网页版不显示
#### 解决：在github仓库里面有，但是无法加载到网页上来，发现可能是加密的问题，只能跑去翻Lupin源代码。在尝试的过程中安装了age、cli、go等等不知道是什么的东西，最后得到了和Handuo大神一样的错误提示……我觉得就到这里，等Lupin作者更新好了。
#### 稍微等了两个小时作者就修好了！真是大神。但是我在报错的情况下坚持加密解密，结果把笔记全部搞乱码了，只能在GitHub目录里翻找加密前的文件，又不会回滚，只能一个一个push上去。最后顺便呢就把今天被加密的几个文件都改了回来，用最安全的不加密+Lupin原始版功能。