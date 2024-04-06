<!--
 * @FilePath: \docs\docs\docsify.md
 * @Date: 2024-04-03 22:25:50
 * @Author: SoulSeven7 xc.xiaoqi7@foxmail.com
 * @LastEditors: SoulSeven7 xc.xiaoqi7@foxmail.com
 * @LastEditTime: 2024-04-05 22:06:25
 * @Description:
-->

# docsify 食用指南 - 简版

## 快速开始

```js
npm i docsify-cli -g // 全局安装

docsify init  // 初始化

docsify serve // 本地预览

```

## loading 提示

```js
、
<!-- index.html -->

<div id="app">加载中</div>
```

## 配置项（部分）

```js
window.$docsify = {

  //  加载自定义导航栏
  loadNavbar: true, // 加载 _navbar.md
  //  loadNavbar: 'nav.md',  // 加载 nav.md

  //  加载自定义侧边栏
  loadSidebar: true,  // 加载 _sidebar.md
  // loadSidebar: 'sidebar.md', // 加载 sidebar.md

  //  自定义侧边栏后默认不会再生成目录，你也可以通过设置生成目录的最大层级开启这个功能。
  subMaxLevel: 2,

  //  切换页面后是否自动跳转到页面顶部。
  auto2top: true,

  //  待测试，本地开发时出错（也许需要线上放在二级目录时生效使用）
  //  文档加载的根路径，可以是二级路径或者是其他域名的路径。
  //  basePath: '/path/',
  //  basePath: 'https://docsify.js.org/', // 直接渲染其他域名的文档

  // 相对路径 , 放在二级目录时不会出现路径错误的问题
  relativePath:true,

  // 启用封面页
  coverpage: true, //  _coverpage.md
  //  coverpage: 'cover.md', // 自定义文件名
  //  coverpage: {   // 多个封面页，并指定文件名
  //    '/': 'cover.md',
  //    '/zh-cn/': 'cover.md',
  //  },

  // 侧边栏中出现的网站图标
  logo: '/_media/icon.svg',
  // 侧边栏标题
  name: '<span>docsify</span>',
  // 作者的写法 style写在index或者新建css文件引入都可
  //  const titleHtml = `
  //  <div class='flex'>
  //    <img src="/assets/logo2.png" class="logo" alt="JoyUp Docs">
  //    <span>JoyUp Docs</span>
  //  </div>
  //  `
  name: titleHtml,

  // 点击左侧标题后跳转的链接地址
  nameLink: '/',

  //  替换主题色。
  themeColor: '#3F51B5'

  //  同时设置 loadSidebar 和 autoHeader 后，可以根据 _sidebar.md 的内容自动为每个页面增加标题
  autoHeader: true,

  //  小屏设备下合并导航栏到侧边栏。
  mergeNavbar: true,

  //  通过 {docsify-updated} 变量显示文档更新日期 // # 实验中，未生效
  formatUpdated: '{MM}/{DD} {HH}:{mm}',

  //  右上角链接打开方式
  cornerExternalLinkTarget: '_blank', // default: '_self'

  //  路由方式
   routerMode: 'history', // default: 'hash'

  //  当设置了routerMode:'history'时，你可能会面临跨域的问题 // # 遇到时再回来处理配置
  crossOriginLinks: ['https://example.com/cross-origin-link'],

  //  只在访问主页时加载封面。
  onlyCover: true,

  //  在找不到指定页面时加载_404.md:
  notFoundPage: true,
};

```

## 插件列表

### 全文搜索 - Search

```js
//  配置项中添加
search: "auto", // 默认值
  (
    //  引入
    <script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
  );
```

### 图片缩放 - Zoom image

```js
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/zoom-image.min.js"></script>
```

### 复制到剪贴板

```js
<script src="//cdn.jsdelivr.net/npm/docsify-copy-code/dist/docsify-copy-code.min.js"></script>
```

### 评论系统支持

```js
  // 配置项添加
  disqus: 'shortname'
  // 引入
  <script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/disqus.min.js"></script>
```

### 字数统计

```js
   count: {
      countable: true,
      fontsize: "0.9em",
      color: "rgb(90,90,90)",
      language: "chinese",
    },

    <script src="//unpkg.com/docsify-count/dist/countable.js"></script>
```

### 使用 emoji

```js
  <script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
```
