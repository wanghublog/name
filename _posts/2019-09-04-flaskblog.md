---
layout: post
title: "Blog by Flask"
date: 2019-9-4
description: "利用flask搭建的一个简单Blog"
tag: Flask
---
   经过一个月的不断上网摸索，终于使用 Flask 初步完成搭建个人博客了，目前该篇 blog 还只能在localhost:5000内运行，我的 Flask 是 1.1.1 版本.
   本篇文章主要展示一下该blog的具体内容以及功能，相关的源码我已经放在[我的GitHub](https://github.com/wanghublog/Flask_Blog)上了。
## 进入虚拟环境
![](/images/posts/flaskblog/start_env.png "运行虚拟环境")
## 进入博客首页
    
    打开浏览器进入： 127.0.0.1:5000

## blog登陆页面展示
![](/images/posts/flaskblog/blog_login.png "登陆页面")
## 第三方QQ登陆展示
![](/images/posts/flaskblog/qq_login.png "QQ登陆")
## celery实现的email功能展示
###window在后台运行：`celery -A celery_runner worker --pool=solo -l info`
![](/images/posts/flaskblog/qq_login.png "celery_mail")
## restful通过HTTP实现对资源操作的操作指令：
###创建token值:`curl -d "username=<username>" -d "password=<password>" http://localhost:5000/api/auth`
###使用token值创建文章:`curl -d "title=<title>" -d "text=<text>" -d "tags=<tag>" -d "token=<token值>" http://localhost:5000/api/posts`
###使用token值删除文章:`curl -X DELETE -d "token=<token值>"http://localhost:8089/api/posts/<post_id>`
###使用token值修改文章:`curl -X PUT -d "title=<new title>" -d "text=<new text>" -d "tags=<new tag>"  -d "token=<token值>" http://localhost:8089/api/posts/<post_id>`
###增加文章例子展示：
![](/images/posts/flaskblog/qq_login.png "restful_test")
## blog首页展示
![](/images/posts/flaskblog/home.png "博客首页")
## blog内容展示
![](/images/posts/flaskblog/blog_detail.png "博客内容")
## 新建blog展示
![](/images/posts/flaskblog/new_post.png "写新博客")
## 编辑blog展示
![](/images/posts/flaskblog/edit_post.png "编辑博客")
## 分页器
![](/images/posts/flaskblog/pager.png "分页器")
## 后台管理展示
![](/images/posts/flaskblog/admin.png "后台管理")
## principal role 功能展示
![](/images/posts/flaskblog/role_need.png "角色功能")

#####  需要源码的在[我的GitHub](https://github.com/wanghublog/flaskblog)获取。


转载请注明原地址，王虎的博客：[https://wanghublog.github.io/](https://wanghublog.github.io/) 谢谢！
