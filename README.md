# eleventy-cn-blog

eleventy-cn-blog是一个开箱即用的静态博客生成器，基于[eleventy](https://www.11ty.dev/)的静态博客生成器，灵感来自[eleventy-base-blog](https://github.com/11ty/eleventy-base-blog)模版，对中文做了一些优化，比如支持中文URL和中文日期格式。该项目尽量使用零js编写，但是由于现实世界和理想之间的巨大落差，有时候不得不尽量克制的添加必要js，如果不需要某些依赖js的功能，也提供删除相关js的方法。如果你喜欢可以点个star，有使用问题可以提交issues
## 示例站点
[demo.xiyu.pro](https://demo.xiyu.pro/)

## 主要特色

- 开箱即用的 Lighthouse 得分为四百分！
- 支持RSS订阅和sitemap生成
- 零js的代码高亮
- 通过短代码优化图像{% image %}
- json格式的文章数据,你甚至可以将静态博客作为api使用(作者本人已实现静态博客对接微信小程序)
  
## 已经增加的功能
- 中文url
- 支持窗口内链接预加载（包含使用不足1kb的js代码）
- 增加分类
- html压缩
- View Transitions页面转换的优雅过渡效果(这个api目前是草案阶段,如需使用需更新谷歌浏览器最新版并开启chrome://flags#view-transition-on-navigation,让我们一同期待View Transitions成为标准)
  
## 如何使用
更详细的文档可以参考 [eleventy](https://www.11ty.dev/) [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog)

1. 克隆或下载本项目到本地
2. 进入项目目录，运行`npm install`安装依赖
3. 运行`npm run serve`启动本地开发服务器
4. 在`_posts`目录下编写你的博客文章，支持Markdown和Nunjucks两种格式
5. 运行`npm run build`生成静态网站文件，输出到`_site`目录
6. 将`_site`目录下的文件部署到你的服务器或托管平台
   
   
## 未来想要实现的功能
-基于Valine的评论功能
-SEO优化
-友情链接页面
-首页改为分页形式
-纯前端搜索功能
-友情链接页面
-持续更新eleventy新版本


## 将项目转为零js博客的步骤
### 去除预加载功能（1kb）
在_includes\layouts\base.njk内删除相关js
![image](https://github.com/xiyuvi/eleventy-cn-blog/assets/38217058/afb4b64a-ed45-4919-860e-2ca5acc25073)

## 注意事项
1.请不要将文章的md文件命名为纯数字/中文/空格，例如1.md，这是因为View Transitions依赖的view-transition-name属性值为纯数字时将为无效值。纯数字的文档名会影响视角过渡效果。后续升级通过修改view-transition-name锚定值解决该问题



