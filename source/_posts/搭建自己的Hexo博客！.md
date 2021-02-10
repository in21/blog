---
title: 搭建自己的Hexo博客！
tags: 技术向
abbrlink: 1439757957
date: 2021-01-24 19:26:41
categories:
  - 教程
---

# 说明

本文将会详细说明使用 Hexo + Netlify 来搭建个人博客，并对主题进行配置。

通过本文的学习，你将收获一个免费、简洁的个人博客，并能够熟悉搭建、写作、部署的全流程。

<!-- more -->

本文在 Ubuntu 20.04 系统下进行。

# 准备

预先安装以下程序：

- [Node.js](http://nodejs.org/)
- [Git](http://git-scm.com/)

如果你已经安装好了，就可以直接前往[安装 Hexo](#安装-Hexo)了。

## 安装 Git

- Windows 下直接前往[官网](https://git-scm.com/download/win)下载即可。
- Linux(Ubuntu/Debian): 执行此命令安装 `sudo apt install git`

## 安装 Node.js

前往 [Node.js 官网](https://nodejs.org/en/download/)下载安装程序，或是前往[国内镜像](https://repo.huaweicloud.com/nodejs/latest/)下载。

其他的安装方法： 使用 [nvs](https://github.com/jasongin/nvs/)。

# 安装 Hexo

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

安装只需要输入这一行命令：
```bash
npm install -g hexo-cli
# or
yarn global add hexo-cli
```
使用 `hexo -v` 验证是否成功。

# 建站

准备好一个放置博客文件的文件夹，然后执行以下命令：
```bash
hexo init <folder>
cd <folder>
npm install # or yarn 
```

`_config.yml` 是站点配置文件，你可以在此配置大部分的参数。

`source` 文件夹是资源文件夹，用于是存放用户资源。

`themes` 是主题文件夹。Hexo 会根据主题来生成静态页面。

到了这里，就可以先看看效果了

```
hexo s
```
然后访问 `localhost:4000` ，可以看到如下效果

![](https://i.loli.net/2021/01/24/RxaklFPZKjO6Jdt.png)

# 部署到 Netlify

登录你的 [Github](https://github.com) 账号，然后创建一个仓库，仓库名任意。

将本地博客文件推送到仓库。

```bash
git init 
git add .
git commit -m "first commit"
git remote add origin <仓库地址>
```
然后推送到仓库

```
git push -u origin master
```

再注册一个 [Netlify](https://www.netlify.com/) 账号进行连接。

- 登录后创建新 Site

![](https://i.loli.net/2021/01/24/3eOVG4UzvYQuhb2.png)

- 连接你的 Github 账户

![](https://i.loli.net/2021/01/24/DQjhWrYfCBIH2cz.png)

- 然后选择你刚才创建的仓库

![](https://i.loli.net/2021/01/24/oj5O1Xtwba2EvNu.png)

- 选择好分支，构建命令后点击 Deploy site

![](https://i.loli.net/2021/01/24/mVkdcbrZj7hXKGB.png)

等构建完成后就可以看到一个链接，这就是你的博客地址了。

![](https://i.loli.net/2021/01/24/gFcPkMqVudmWo2p.png)



