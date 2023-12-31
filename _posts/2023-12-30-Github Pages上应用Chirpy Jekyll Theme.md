---
layout: post
title:  "Github Pages上应用Chirpy Jekyll Theme"
date:   2023-12-30 22:59:27 +0800
categories: jekyll
---

### 参考链接
* Chirpy Jekyll Theme (https://github.com/cotes2020/jekyll-theme-chirpy)
* Chirpy Jekyll Theme的4篇使用介绍，即Demo (https://chirpy.cotes.page/posts/getting-started/)
* Chirpy Jekyll Theme的Chirpy Starter (https://github.com/cotes2020/chirpy-starter)

### Jekyll基础环境安装
Follow the instructions in the [Jekyll Docs](https://jekyllrb.com/docs/installation/) to complete the installation of the basic environment. [Git](https://git-scm.com/) also needs to be installed.
* Windows 11 上用RubyInstaller安装
* 安装Node.js 

### Github上建立一个新仓库，采用Option 1，便于更新
There are two ways to create a new repository for this theme:

- [**Using the Chirpy Starter**](#option-1-using-the-chirpy-starter) - Easy to upgrade, isolates irrelevant project files so you can focus on writing.
- [**GitHub Fork**](#option-2-github-fork) - Convenient for custom development, but difficult to upgrade. Unless you are familiar with Jekyll and are determined to tweak or contribute to this project, this approach is not recommended.

#### Option 1. Using the Chirpy Starter

Sign in to GitHub and browse to [**Chirpy Starter**][starter], click the button <kbd>Use this template</kbd> > <kbd>Create a new repository</kbd>, and name the new repository `USERNAME.github.io`, where `USERNAME` represents your GitHub username.

#### Option 2. GitHub Fork

Sign in to GitHub to [fork **Chirpy**](https://github.com/cotes2020/jekyll-theme-chirpy/fork), and then rename it to `USERNAME.github.io` (`USERNAME` means your username).

### Git远程仓库到本地 For Installing Dependencies
* git clone后有了如下目录 C:\Users\XXX\Documents\blog\Jekyll\xxx.github.io 写了新的post后，在这个目录的_post中

* Before running local server for the first time, go to the root directory of your site and run:

```console
$ bundle
```
### Running Local Server

* cd ./xxx.github.io

You may want to preview the site contents before publishing, so just run it by:

```console
$ bundle exec jekyll s
```

After a few seconds, the local service will be published at _<http://127.0.0.1:4000>_.

### Deploy by Using GitHub Actions

There are a few things to get ready for.

- If you're on the GitHub Free plan, keep your site repository public.
- If you have committed `Gemfile.lock`{: .filepath} to the repository, and your local machine is not running Linux, go the the root of your site and update the platform list of the lock-file:

```console
$ bundle lock --add-platform x86_64-linux
```

Next, configure the _Pages_ service.

1. Browse to your repository on GitHub. Select the tab _Settings_, then click _Pages_ in the left navigation bar. Then, in the **Source** section (under _Build and deployment_), select [**GitHub Actions**][pages-workflow-src] from the dropdown menu.  

2. Push any commits to GitHub to trigger the _Actions_ workflow. In the _Actions_ tab of your repository, you should see the workflow _Build and Deploy_ running. Once the build is complete and successful, the site will be deployed automatically.

At this point, you can go to the URL indicated by GitHub to access your site.


### Push Changes to Github

* git pull  #第一次push前和远程仓库同步
* git add . #有变更后
* git status
* git commit -m ' 提交信息'
* git remote add origin git@github.com:xxx/xxx.github.io.git
* git push -u origin main  #从Chirpy Starter建立的仓库默认Branch是main，不是常见的master



### 插件及设置


### 写作



