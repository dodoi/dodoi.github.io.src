---
title: hexo项目引用模板不能提交问题 submodule问题
date: 2017-01-19 17:18:21
tags: [杂项]
---
hexo 生成的博客，引入新的模板
 ```
  git clone https://github.com/wuchong/jacman.git themes/jacman

 ```
项目提交git,出现异常
```
The page build failed with the following error:

The submodule `themes/jacman` was not properly initialized with a `.gitmodules` file. For more information, see https://help.github.com/articles/page-build-failed-missing-submodule/.

For information on troubleshooting Jekyll see:

  https://help.github.com/articles/troubleshooting-jekyll-builds

If you have any questions you can contact us by replying to this email.
```

问题通过submodule命令解决
```
git submodule add https://github.com/wuchong/jacman.git themes/jacman
```
当前工程根路径下生成一个名为“.gitmodules”的文件
```
[submodule "themes/jacman"]
	path = themes/jacman
	url = https://github.com/wuchong/jacman.git
```
描述了子模块的信息