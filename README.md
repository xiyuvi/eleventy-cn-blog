# eleventy-cn-blog

eleventy-cn-blog是一个开箱即用的静态博客生成器，基于[eleventy](https://www.11ty.dev/)的静态博客生成器，灵感来自[eleventy-base-blog](https://github.com/11ty/eleventy-base-blog)模版，对中文做了一些优化，比如支持中文URL和中文日期格式。

支持环保事业,减少用户设备能耗,该项目尽量克制使用js编写，但是由于现实世界和理想之间的巨大落差，有时候不得不添加必要js，如果不需要某些依赖js的功能，可以手动删除相关js不影响整体使用。如果喜欢可以点个star，有使用问题可以提交issues
## 示例站点
[demo.xiyu.pro](https://demo.xiyu.pro/)
![image](https://github.com/xiyuvi/eleventy-cn-blog/assets/38217058/6f5bf2aa-f644-4415-a3ea-aacd47f293c6)


## 主要特色功能

- [x] 开箱即用的 Lighthouse 得分为四百分！
      
![image](https://github.com/xiyuvi/eleventy-cn-blog/assets/38217058/b2e6cd4c-1d64-4de9-ba97-6facd2da04cb)

- [x] 支持RSS订阅和sitemap生成
- [x] 代码高亮
- [x] 通过短代码优化图像{% image %}
- [x] json格式的文章数据,你甚至可以将静态博客作为api使用(作者本人已实现静态博客对接微信小程序)
- [x] 支持中文url（url本来就支持中文，是11ty内置的url美化插件不支持中文导致的问题，这里直接不使用插件就解决了问题）
- [x] 支持窗口内链接预加载（包含4kb的js）
- [x] 增加分类
- [x] html压缩
- [x] View Transitions页面转换的优雅过渡效果(这个api目前是草案阶段,如需使用需更新谷歌浏览器最新版并开启chrome://flags#view-transition-on-navigation,一同期待View Transitions成为标准)
- [x] 支持Service Worker,博客可以在无网环境使用（包含少量js）
      
![image](https://github.com/xiyuvi/eleventy-cn-blog/assets/38217058/76c75ad5-4ed4-4d7e-a74c-77193da73aee)


  
## 如何使用
更详细的文档可以参考 [eleventy](https://www.11ty.dev/) [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog)

1. 克隆或下载本项目到本地
2. 进入项目目录，运行`npm install`安装依赖
3. 运行`npm run serve`启动本地开发服务器
4. 在`_posts`目录下编写你的博客文章，支持Markdown和Nunjucks两种格式
5. 运行`npm run build`生成静态网站文件，输出到`_site`目录
6. 将`_site`目录下的文件部署到你的服务器或托管平台
   
   
## 未来想要实现的功能

- [ ]  基于Valine的评论功能
- [ ]  SEO优化
- [ ]  友情链接页面
- [ ]  首页改为分页形式
- [ ]  纯前端搜索功能
- [ ]  友情链接页面
- [ ]  持续更新eleventy新版本


## 注意事项
1.不要将文章的md文件命名为纯数字/中文/空格，例如1.md，这是因为View Transitions依赖的view-transition-name属性值为纯数字时将为无效值。纯数字的文档名会影响视角过渡效果。后续升级通过修改view-transition-name锚定值解决该问题



