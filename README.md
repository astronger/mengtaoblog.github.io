# hexo+Anisina+github ����˲���
# ��
[Hexo](https://hexo.io/zh-cn/%22) ��һ���ǻ��� node.js �Ŀ��١�����Ҹ�Ч�Ĳ��Ϳ�ܡ�[Anisina](https://haojen.github.io/2017/05/09/Anisina-%E4%B8%AD%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B/) ��һ�� hexo �����⣬��࣬���ˣ���Ҳ�Ǳ���ѡ����������ԭ��
# ����
���Բο� [Hexo](https://hexo.io/zh-cn/%22) �Ĺ�������Ӧ������Ҫ node �� git ��Ҳ���ٶ�˵���ο��ٷ��̳���� hexo �İ�װ��
[Anisina](https://haojen.github.io/2017/05/09/Anisina-%E4%B8%AD%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B/)  �İ�װҲ��ο��ٷ��Ľ̳̣�������Ҫ˵���ǹ��� Anisina �������ļ���
## Anisina ������
�� _config.yml �����޸ģ�

```xml
#���ǻ��������� ������Ҳ�ܿ������� Ҳ���Բο��ٷ�����
title: ���� # your blog title name
subtitle:  
author: ���� # ����
language: zh-CN
timezone: Asia/Shanghai
SEOTitle: ����'s blog #���⣬Ҳ���ǲ������Ͻǵ��Ǹ�
header-img: /image/header.jpg  #�����Լ������ļ��з�����ļ��������˵��ôŪ��
email: 
description: "��¼ѧϰ�Ĺ���"
keyword: # seo key words
favicon: /image/header.jpg #��key��ʾ
```
## �����
��������ã�
```
    sidebar: true
    sidebar-about-description: "�����ֵ��Ӯ������" # ��������
    sidebar-avatar: /image/header.jpg    # ͷ��ͼƬ����ʹ�õ�����˵�����ַ�ʽ���õ�
    zhihu_username: yourname # �����������������ļ�������еģ�ֻ��Ҫ�����������罻�˻������ƾͿ��ԣ����������Ӧ��ͷ���ʱ�򣬻��Զ���ͨ���ӿڵķ�ʽ��λ�������˻�ҳ��
    github_username: yourname 
    #�����ǹ��ڱ�ǩ�����ã�֮ǰ�Ҿʹ��ڱ�ǩ����ʾ����������������Ĭ����1���ĳ�0�Ϳ�����
    featured-tags: true
    featured-condition-size: 0
    #������ʾ��ע��ʹ��json�ķ�ʽ
    friends: [
        {
            title: "CSDN",
            href: "https://blog.csdn.net/ourstronger"
        },
        {
            �����İ�������ķ�ʽ��������...
        }
    ]

```


���벩�͵ĸ�Ŀ¼���е�source�ļ����У�����һ���ļ��У�����ȡ��img����image�������ľͺá�
Ȼ���ͼƬ�������У�ȡͼƬ��ʱ��ʹ����Ŀ�ľ���·���������ļ��е�������img������ͼƬ��ʱ��
ֻ��Ҫ/img/xxx.jpg,�����ķ�ʽ�Ϳ���ȡ����

## ����
#### ����һ�� Tags ����ҳ�棺
��������:hexo new page "Tags" , ����ڲ��͵� source Ŀ¼������һ����Ϊ Tags ���ļ��У��������һ�� index.md ��ʽ��ҳ�棬���û�����ֶ�����.
Ȼ��� yourblog/source �ļ��У��ҵ� Tags/index.md ����ļ���Ȼ�������������� --- ���棬ָ��һ�� layout: tags ֵ��ע�� key �� value ֮��Ŀո�
Ȼ����������������ɲ�������: **hexo clean** && **hexo g** , Ȼ��������� **hexo s** �ڱ��ز鿴Ч����

![imge](https://img-blog.csdnimg.cn/c3bfe25440824381bcdb6b02d3aba885.png)
## ����
����һ�����ģ�

```bash
hexo new "your-post-name
```
�ڴ����õ����µ�ͷ�������������ã�

```yaml
---
layout: post
title:  hi 2020
subtitle: 'hi, I''m ����'
author: ����
header-img: ''
cdn: header-on
tags:
  - java
  - mysql
date: 2020-01-01 00:00:00
---
```

## ����
��� [������](https://www.livere.com/) ����ϵͳ��������Ҫ���ȥע�ᣬȻ��װ��ѡ����Ѱ�ģ��м�Ĺ��̾�ʡ���ˣ�����������½��棺

![���������ͼƬ����](https://img-blog.csdnimg.cn/cd1877c421754577a4e8cc1947e5977f.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L291cnN0cm9uZ2Vy,size_16,color_FFFFFF,t_70)
����ͼ��Ȧ������ uid ��������_config.yml �����������ã�

```yaml
    use_livere: ture
    livere_uid: your uid
```
## ͳ����
��������ɹ����������˵˵��վ����ķ��������ÿͺ����µ��Ķ�����������չ����:

����ʹ�õ��� [������](http://busuanzi.ibruce.info/) �ṩ���Ķ�ͳ�ƹ���:

���������µ� layout/_partial/footer.ejs

������´��룺

```yaml
<span id="busuanzi_container_site_pv"" style="font-size: 12px;display:none;">�ܷ�������<span id="busuanzi_value_site_pv"></span>��</span>
<span class="post-meta-divider">|</span>
<span id="busuanzi_container_site_uv" style="font-size: 12px;display:none;">�ܷÿͣ�<span id="busuanzi_value_site_uv"></span>��</span>

```
�������������ͷÿ;�����ˣ�

��������µ��Ķ�����
���������µ� layout/post.ejs

���� class="tags text-center"��������λ�ý������ã�

![���������ͼƬ����](https://img-blog.csdnimg.cn/8125ff6bae2348afa7a240fc923fd500.png)

```yaml
<br/><span id="busuanzi_container_page_pv" style="display:none;">�Ķ�����
<span id="busuanzi_value_page_pv"></span>��</span>
```

## ����
�����ڣ���֪�����Ĳ����Ƿ�ﵽ����ϣ����Ч����������ԵĻ����������Ҿ���˵˵����ɣ�

������ʹ�õ��� github , ������Ҫ���������½��洴��һ���ֿ⣺

![���������ͼƬ����](https://img-blog.csdnimg.cn/351d1107cd264e2786eaef3e3d6b9e07.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L291cnN0cm9uZ2Vy,size_16,color_FFFFFF,t_70)
����Ҫ���ľ������ã�

������_config.yml �޸��������ã�

```yaml
deploy:
   type: git  
   repo: 
   github: your address #���Ĳֿ��ַ
branch: master #�ύ�ķ�֧
```
������Ϻ�ʹ������������� github��

```yaml
hexo clean
hexo g
hexo s #�ȱ��������ַ�鿴һ���Ƿ����Լ������ctrl+c����
hexo d #����Զ����
```

��Ȼ��Ҳ���Բ����ڱ��ز鿴��ֱ��ִ���������

```yaml
hexo g --d #ֱ�����ɾ�̬��Դ�����Ͳ���Զ�ֿ̲�
```

���ʱ���������´���
```yaml
ERROR Deployer not found: git��
```

��Ҫ��װ hexo-deployer-git��ִ����������
```yaml
 npm install hexo-deployer-git --save
 ```

�ٴ����ͣ�
```yaml
hexo d
```

���ˣ�������ǰע�������������github����ѡ�� https .

�������治��Ҫʹ���Լ���������ʱ����ʹ�� github Ĭ��������ʱ��ֻ��Ҫ�� CNAME �ļ�ɾ�������²���һ�� ok �ˣ�������ֲ������ʲ��˵��������һ��������Ļ��档���ϡ�

### ��Ʒչʾ�� [http://www.itmengtao.cn](http://www.itmengtao.cn)
