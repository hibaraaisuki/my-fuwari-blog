---
title: Astro本地调试
published: 2026-03-12
description: 记录一下本地调试的常用命令。
image: "./cover.jpg"
tags: [Astro]
category: 笔记
draft: true
---

## 🖥️ 启动开发服务器

1. 打开git bash，进入项目根目录。
2. 输入命令`pnpm run dev`启动Astro开发服务器，等待运行成功。
3. 打开浏览器，输入"`http://localhost:4321/`"即可访问。
:::note
可以实时修改代码和内容，网页会自动刷新，马上可以预览修改后的效果。
:::

**启动开发服务器**
```bash
pnpm run dev
```

**等待启动**
```
$ pnpm run dev

> fuwari@0.0.1 dev D:\github\my-fuwari-blog
> astro dev

14:50:02 [types] Generated 2ms
14:50:03 [content] Syncing content
14:50:03 [content] Synced content

 astro  v5.13.10 ready in 6543 ms

┃ Local    http://localhost:4321/
┃ Network  use --host to expose

14:50:03 watching for file changes...
```

**预览**
![浏览器示例图片](./example-localhost.png "浏览器示例图片")


## 🔧 退出开发服务器

在git bash上键入`CTRL + C`退出开发服务器，根据提示输入`Y`或`N`即可。