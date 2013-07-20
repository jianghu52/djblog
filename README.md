介绍
----
一个基于 django 开发的 blog 程序，演示站点：[ichuan.net][1]。特性包括：

  1. HTML5
  2. 手持设备访问优化
  3. Disqus 评论系统集成
  4. Markdown 语法写作
  5. 标签
  6. 单页面
  7. 友情链接
  8. Google Analytics 集成
  9. 主题
  10. RSS
  11. Google 自定义搜索

依赖
----

1. markdown: `https://github.com/waylan/Python-Markdown/`
2. django >= 1.3

安装步骤
--------

1. 创建数据库，例如 mysql 数据库：`$ mysql -u root -proot -e 'create database blog'`
2. 拷贝 `local_settings.default.py` 为 `local_settings.py`，修改里面的数据库配置。还有其他配置可以改
3. 执行 `python manage.py syncdb` 同步数据库(这里对新手要注意，从github下载下来的zip文件是djblog-master，需要改成djblog文件夹，这样执行syncdb才不会出错。另外，先要安装markdown插件，之后再执行syncdb）
4. 执行 `python manage.py runserver 0.0.0.0:8000` 启动临时服务器（如果你之间配置过了python，那么可能只需要输入
python manage.py runserver 就可以了。不需要再硬设置端口，因为有可能被占用）
5. 浏览器访问 `http://localhost:8000`，后台地址是 `http://localhost:8000/admin/`，口令在第 `3` 步时创建
6. 在后台的`sites`里更改默认的`example.com`为你自己的域名（`RSS`输出中的链接会使用到）（这步不改也行，反正现在googlereader已死-_-!)


自定义主题
----------

主题放在 `templates/` 目录下，一个目录是一个主题，`classic` 为默认主题，可参考这个制作新主题。
PS 原始版本在ichuan的项目中，这里为表示尊敬，连基本的logo都没有改变，只是为了保证新手能一定使用的包修改了一下readme

[1]: http://ichuan.net
[2]: 这个版本取自ichuan的git，连基本的logo都没改变。只是因为自己是纯新手，而且没有指导，只能自己摸索。

