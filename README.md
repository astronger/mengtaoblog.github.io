# hexo+Anisina+github 搭建个人博客
# 起步
[Hexo](https://hexo.io/zh-cn/%22) 是一个是基于 node.js 的快速、简洁且高效的博客框架。[Anisina](https://haojen.github.io/2017/05/09/Anisina-%E4%B8%AD%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B/) 是一个 hexo 的主题，简洁，明了，这也是本人选择这个主题的原因。
# 下载
可以参考 [Hexo](https://hexo.io/zh-cn/%22) 的官网，对应环境需要 node 和 git 我也不再多说，参考官方教程完成 hexo 的安装；
[Anisina](https://haojen.github.io/2017/05/09/Anisina-%E4%B8%AD%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B/)  的安装也请参考官方的教程，下面我要说的是关于 Anisina 的配置文件；
## Anisina 的配置
打开 _config.yml 进行修改：

```xml
#这是基本的配置 看名字也能看出含义 也可以参考官方解释
title: 李多多 # your blog title name
subtitle:  
author: 李多多 # 作者
language: zh-CN
timezone: Asia/Shanghai
SEOTitle: 李多多's blog #标题，也就是博客左上角的那个
header-img: /image/header.jpg  #我是自己建的文件夹放入的文件，待会会说怎么弄的
email: 
description: "记录学习的过程"
keyword: # seo key words
favicon: /image/header.jpg #如key所示
```
## 侧边栏
侧边栏配置：
```
    sidebar: true
    sidebar-about-description: "创造价值，赢得尊重" # 个人描述
    sidebar-avatar: /image/header.jpg    # 头像，图片就是使用的上面说的那种方式配置的
    zhihu_username: yourname # 这是下载主题下来文件里面就有的，只需要配上您各个社交账户的名称就可以，当您点击对应的头像的时候，会自动的通过接口的方式定位到您的账户页面
    github_username: yourname 
    #下面是关于标签的配置，之前我就存在标签不显示的情况，他这个好像默认是1，改成0就可以了
    featured-tags: true
    featured-condition-size: 0
    #如题所示，注意使用json的方式
    friends: [
        {
            title: "CSDN",
            href: "https://blog.csdn.net/ourstronger"
        },
        {
            其他的按照上面的方式进行配置...
        }
    ]

```


进入博客的根目录下中的source文件夹中，建立一个文件夹，随您取名img或者image，您开心就好。
然后把图片放入其中，取图片的时候使用项目的绝对路径，加入文件夹的名称是img，您用图片的时候
只需要/img/xxx.jpg,这样的方式就可以取到。

## 顶部
#### 创建一个 Tags 导航页面：
运行命令:hexo new page "Tags" , 这会在博客的 source 目录下生成一个名为 Tags 的文件夹，里面会有一个 index.md 格式的页面，如果没有请手动创建.
然后打开 yourblog/source 文件夹，找到 Tags/index.md 这个文件，然后设置在两条的 --- 里面，指定一个 layout: tags 值。注意 key 和 value 之间的空格
然后运行命令，重新生成博客内容: **hexo clean** && **hexo g** , 然后可以运行 **hexo s** 在本地查看效果。

![imge](https://img-blog.csdnimg.cn/c3bfe25440824381bcdb6b02d3aba885.png)
## 文章
创建一条博文：

```bash
hexo new "your-post-name
```
在创建好的文章的头部加入以下配置：

```yaml
---
layout: post
title:  hi 2020
subtitle: 'hi, I''m 李多多'
author: 李多多
header-img: ''
cdn: header-on
tags:
  - java
  - mysql
date: 2020-01-01 00:00:00
---
```

## 评论
添加 [来比力](https://www.livere.com/) 评论系统，首先需要大家去注册，然后安装，选择免费版的，中间的过程就省略了，最后来到以下界面：

![在这里插入图片描述](https://img-blog.csdnimg.cn/cd1877c421754577a4e8cc1947e5977f.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L291cnN0cm9uZ2Vy,size_16,color_FFFFFF,t_70)
复制图中圈起来的 uid 来到您的_config.yml 进行以下配置：

```yaml
    use_livere: ture
    livere_uid: your uid
```
## 统计量
在搜索完成过后接下来该说说网站下面的访问量、访客和文章的阅读量是怎样扩展的了:

这里使用的是 [不蒜子](http://busuanzi.ibruce.info/) 提供的阅读统计功能:

进入主题下的 layout/_partial/footer.ejs

添加以下代码：

```yaml
<span id="busuanzi_container_site_pv"" style="font-size: 12px;display:none;">总访问量：<span id="busuanzi_value_site_pv"></span>次</span>
<span class="post-meta-divider">|</span>
<span id="busuanzi_container_site_uv" style="font-size: 12px;display:none;">总访客：<span id="busuanzi_value_site_uv"></span>人</span>

```
这样，访问量和访客就完成了；

下面就文章的阅读量：
进入主题下的 layout/post.ejs

搜索 class="tags text-center"，在以下位置进行配置：

![在这里插入图片描述](https://img-blog.csdnimg.cn/8125ff6bae2348afa7a240fc923fd500.png)

```yaml
<br/><span id="busuanzi_container_page_pv" style="display:none;">阅读量：
<span id="busuanzi_value_page_pv"></span>次</span>
```

## 部署
到现在，不知道您的博客是否达到了您希望的效果，如果可以的话，接下来我就在说说部署吧！

我这里使用的是 github , 首先需要您来到以下界面创建一个仓库：

![在这里插入图片描述](https://img-blog.csdnimg.cn/351d1107cd264e2786eaef3e3d6b9e07.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L291cnN0cm9uZ2Vy,size_16,color_FFFFFF,t_70)
下面要做的就是配置；

打开您的_config.yml 修改以下配置：

```yaml
deploy:
   type: git  
   repo: 
   github: your address #您的仓库地址
branch: master #提交的分支
```
配置完毕后使用以下命令，部署到 github：

```yaml
hexo clean
hexo g
hexo s #先本地输入地址查看一下是否是自己满意的ctrl+c结束
hexo d #部署到远处仓
```

当然您也可以不存在本地查看，直接执行以下命令：

```yaml
hexo g --d #直接生成静态资源并推送部署到远程仓库
```

这个时候会出现以下错误：
```yaml
ERROR Deployer not found: git。
```

需要安装 hexo-deployer-git，执行以下命令
```yaml
 npm install hexo-deployer-git --save
 ```

再次推送：
```yaml
hexo d
```

至此，将你提前注册的域名解析至github，可选择 https .

当您后面不需要使用自己的域名的时候想使用 github 默认域名的时候只需要把 CNAME 文件删除再重新部署一次 ok 了，如果发现部署后访问不了的情况请清一下浏览器的缓存。以上。

### 成品展示： [http://www.itmengtao.cn](http://www.itmengtao.cn)
