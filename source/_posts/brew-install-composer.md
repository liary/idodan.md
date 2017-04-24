---
title: brew install composer
date: 2017-04-24 15:27:48
tags: 'PHP'
---
新公司用的是php的yii2框架，因此推进一些旧项目的前后分离需要了解一下yii相关的东西
## 配置环境
由于Mac自带了php5.6，因此只需安装php包管理器composer，现在记录下类似以及神似npm的composer安装遇到的坑：
- 使用命令`brew install composer`遇到`Please delete these paths and run brew update.Error: Could not link:/usr/local/share/zsh/site-functions/_brew`系列的报错
- 错误类型2：`Could not symlink bin/libpng-config`

## 解决方法
- 针对第一种好办，依照指示`rm -rf`依次把相关的东东删掉
- 第二个报错网上给的方法很多，真正实用的是`brew link --overwrite freetype`

## yii2浅见
yii2里有很多东西类似react，至少强行用react的思路去理解入门教程没遇到问题，这个结论等composer安装完启动demo才可以下定论，无论如何，至少证明了现在前端确确实实反哺了其它语言，一如npm于composer，一如我脑补中的action于yii2里的action function(可能是反过来)，以后面对node黑的质疑又多了一个呵呵哒的理由了