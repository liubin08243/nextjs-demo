# Next.js 演示项目

这是一个简单的 Next.js 演示项目模板，默认显示 "Hello World"。

## 开始使用

首先，安装依赖：

```bash
npm install
```

然后，运行开发服务器：

```bash
npm run dev
```

打开 [http://localhost:3000](http://localhost:3000) 查看结果。

## 项目结构

- `src/app/page.tsx` - 主页组件
- `src/app/layout.tsx` - 全局布局组件
- `Dockerfile` - Docker镜像构建配置
- `.github/workflows/docker-build.yml` - GitHub Actions自动构建工作流

## 技术栈

- [Next.js](https://nextjs.org/) - React 框架
- [React](https://reactjs.org/) - JavaScript 库
- [TypeScript](https://www.typescriptlang.org/) - JavaScript 的超集
- [Tailwind CSS](https://tailwindcss.com/) - CSS 框架
- [Docker](https://www.docker.com/) - 容器化部署
- [GitHub Actions](https://github.com/features/actions) - CI/CD工作流

## Docker部署

### 本地构建和运行

在本地构建Docker镜像：

```bash
docker build -t nextjs-demo .
```

运行Docker容器：

```bash
docker run -p 3000:3000 nextjs-demo
```

### 使用GitHub容器注册表

本项目配置了GitHub Actions自动构建工作流。当您推送代码到main分支时，会自动构建Docker镜像并发布到GitHub容器注册表。

从GitHub容器注册表拉取并运行镜像：

```bash
# 替换 {username} 为您的GitHub用户名
docker pull ghcr.io/{username}/nextjs-demo:latest
docker run -p 3000:3000 ghcr.io/{username}/nextjs-demo:latest
```

## 注意事项

确保您的GitHub仓库已启用GitHub Actions，并且允许写入包权限。

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
