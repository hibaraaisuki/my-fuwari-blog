# 🍥 [my-fuwari-blog]

> 基于 [Fuwari](https://github.com/saicaca/fuwari) 主题构建的个人博客 —— 一个使用 [Astro](https://astro.build) 和 [Tailwind CSS](https://tailwindcss.com) 打造的静态博客站点。

本仓库是我在 Fuwari 主题基础上进行个性化创作和内容维护的地方，同时也会定期同步上游原作者的更新，保持主题的活力。

![预览图](./readme-example.png)  

## ✨ 特性

- ✅ 基于 Astro 4.0 + Tailwind CSS，极速加载
- ✅ 暗色模式支持
- ✅ 响应式设计，移动端友好
- ✅ 文章分类、标签系统
- ✅ 内置搜索功能
- ✅ RSS 订阅、Sitemap 自动生成
- ✅ 评论系统集成（如 Giscus、Twikoo 等）
- ✅ 可自定义主题配色、字体
- ✅ 易于部署（支持 GitHub Pages、Netlify、Vercel 等）

## 🚀 快速开始

### 前置要求

- Node.js 18+
- pnpm 推荐（也可使用 npm / yarn）

### 克隆仓库

```bash
git clone blog-dev https://github.com/hibaraaisuki/my-fuwari-blog.git
cd my-fuwari-blog
```

### 安装依赖

```bash
pnpm install
# 或 npm install
```

### 本地开发

```bash
pnpm dev
# 或 npm run dev
```

启动后访问 `http://localhost:4321` 即可预览。

### 构建静态文件

```bash
pnpm build
# 构建产物位于 dist/ 目录，可直接部署
```

## ⚙️ 配置说明

### 基础配置

博客的基础信息（站点标题、作者、语言等）在 `src/config.ts` 中修改：

```ts
export const SITE = {
  title: '你的博客名',
  description: '博客描述',
  defaultLanguage: 'zh-CN',  // 或 en
};

export const AUTHOR = {
  name: '你的名字',
  avatar: '/avatar.png',      // 头像路径
  bio: '个人简介',
};
```

### 主题定制

- 配色、字体等样式在 `src/styles/` 中调整。
- 导航菜单、社交链接等在 `src/config.ts` 的相应位置修改。
- 评论插件配置也在 `src/config.ts` 中启用和填写参数。

更多自定义可参考 [Fuwari 官方文档](https://github.com/saicaca/fuwari)。

## 📦 部署

你可以将博客部署到任何静态托管服务。下面以 GitHub Pages 为例：

1. 在仓库设置中启用 GitHub Pages，并选择 `GitHub Actions` 作为构建来源。
2. 在本地运行 `pnpm build`，将 `dist/` 内容推送到仓库（或使用 CI 自动构建）。

## 🔄 同步上游更新

由于本仓库派生自 Fuwari，你可以通过以下步骤拉取原主题的最新改动：

```bash
# 添加原仓库为 upstream（只需执行一次）
git remote add upstream https://github.com/saicaca/fuwari.git

# 拉取上游更新
git fetch upstream

# 合并到你的主分支（假设当前在 main 分支）
git merge upstream/main --allow-unrelated-histories

# 解决冲突后提交
```

建议定期检查上游更新，以获取新功能和安全修复。

## 📄 许可证

本项目基于 Fuwari 主题构建，Fuwari 采用 [MIT 许可证](LICENSE)。  
你可以在遵守原许可证的前提下自由使用、修改和分享。

---

如果你觉得这个主题不错，别忘了给 [Fuwari 原项目](https://github.com/saicaca/fuwari) 点个 ⭐ 哦！  
也欢迎在下方评论区或 Issues 中交流你的创作心得。