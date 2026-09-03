# 慢慢写 · Astro 博客

这是一个部署在 Cloudflare 上的 Astro 博客，文章位于 `src/content/posts/`。

## 评论系统

文章页使用 Giscus 保存评论。启用评论前，请：

1. 将 GitHub 仓库 `wubt/blog` 设置为公开；
2. 在仓库设置中启用 Discussions，并确保存在 `General` 分类；
3. 打开 [giscus.app](https://giscus.app/)，输入 `wubt/blog` 获取配置；
4. 将 `repo-id` 和 `category-id` 写入 `.env`：

```env
PUBLIC_GISCUS_REPO_ID=你的_repo_id
PUBLIC_GISCUS_CATEGORY_ID=你的_category_id
```

然后重新部署：

```sh
npm run deploy
```

没有配置这两个变量时，文章页会显示配置提示，不会加载评论脚本。

```sh
npm create astro@latest -- --template minimal
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
