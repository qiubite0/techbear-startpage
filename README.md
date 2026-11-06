# 科技熊 DIY 导航 · TechBear Startpage

**把你的收藏，变成你的主页。**

[展示官网](https://qiubite0.github.io/techbear-startpage/) · [在线示例](https://qiubite0.github.io/techbear-startpage/demo/) · [下载扩展](https://github.com/qiubite0/techbear-startpage/releases/latest)

免费开源、无广告、每个人使用自己的收藏。

本地优先、零构建依赖的 DIY 浏览器主页，支持 Edge / Chrome Manifest V3 与普通静态网页。

## 功能
- 导航站式分类、搜索、网站卡片；浅色/深色主题、紧凑布局、动态渐变。
- 自定义主页名称，添加链接，JSON 导入导出（备份含私人收藏，请自行保管）。
- 可选连接浏览器收藏夹：默认按用途自动分类，也可保留原文件夹分类；单独授权读取本机网站图标；右键确认删除单条收藏并同步，不按 URL 批量删除。
- 无埋点、无账户、无云上传、无第三方依赖。默认只含三个公开示例。

## 安装
下载本仓库 ZIP 并解压，打开 `edge://extensions` 或 `chrome://extensions`，打开开发人员模式，加载解压目录。新标签页提示更改时保留扩展。点击“连接收藏夹”才会请求 bookmarks/favicon 权限。

## 网页使用
在目录运行 `python -m http.server 8080`，打开 http://localhost:8080 。网页版本支持本地配置，不能访问浏览器收藏夹。

## 开发与验证
Node.js 20+；`npm test`、`npm run check`。无需 npm install。修改 HTML/CSS/JS 即可。在扩展管理页重新加载后刷新新标签页。

## 数据与边界
设置使用 localStorage，仅限当前浏览器配置。浏览器模式遵循原收藏夹分类；DIY 本地模式可以自建分类。备份导入只替换本地配置，不导入浏览器收藏夹。删除不可在应用内撤销。没有实现拖拽排序或云同步。可执行与 file URL 不收录。

## 参考与致谢
交互思路参考 [Bonjourr](https://github.com/victrme/Bonjourr) 的本地优先体验、[Tabliss](https://github.com/joelshepherd/tabliss) 的自定义布局、[nightTab](https://github.com/zombieFox/nightTab) 的分组与备份；信息架构参考 Tbox / AIGC.cn 工具导航。独立实现，未复制上述项目代码、图标或其他资源。本仓库不包含作者私人收藏及个人 Logo，品牌名称可在设置中修改。

MIT License。
