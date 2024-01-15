# eleventy-cn-blog

eleventy-cn-blog是一个开箱即用的静态博客生成器，基于[eleventy](https://www.11ty.dev/)的静态博客生成器，灵感来自[eleventy-base-blog](https://github.com/11ty/eleventy-base-blog)模版，对中文做了一些优化，比如支持中文URL和中文日期格式。该项目尽量使用零js编写，但是由于现实世界和理想之间的巨大落差，有时候不得不尽量克制的添加必要js，如果不需要某些依赖js的功能，也提供删除相关js的方法。如果你喜欢可以点个star，有使用问题可以提交issues

## 主要功能

- 开箱即用的 Lighthouse 得分为四百分！
- 支持RSS订阅和sitemap生成
- 零js的代码高亮
- 通过短代码优化图像{% image %}
  
## 基于eleventy-base-blog增加的功能
- 中文url
- 支持窗口内链接预加载（包含使用不足1kb的js代码）
- 增加分类
- html压缩
  
## 如何使用
更详细的文档可以参考 [eleventy](https://www.11ty.dev/) [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog)

1. 克隆或下载本项目到本地
2. 进入项目目录，运行`npm install`安装依赖
3. 运行`npm run serve`启动本地开发服务器
4. 在`_posts`目录下编写你的博客文章，支持Markdown和Nunjucks两种格式
5. 运行`npm run build`生成静态网站文件，输出到`_site`目录
6. 将`_site`目录下的文件部署到你的服务器或托管平台
   
   
## 未来想要实现的功能

SEO优化
开箱即用的友情链接页面
使用View Transitions API创建的优雅过渡效果
持续更新eleventy新版本

## 将项目转为零js博客的步骤
### 去除预加载功能（1kb）
在_includes\layouts\base.njk内删除相关js
![image](https://github.com/xiyuvi/eleventy-cn-blog/assets/38217058/afb4b64a-ed45-4919-860e-2ca5acc25073)



