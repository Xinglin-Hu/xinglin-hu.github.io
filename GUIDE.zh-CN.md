# Xinglin Hu 个人主页：GitHub 网页上传与维护指南

这个网站的所有公开页面使用英文；本指南使用中文。网站以 GitHub Pages 自带的 Jekyll 生成，初次上传后，日常更新直接在 GitHub 网页中完成。你不需要安装开发软件、运行命令或使用 Cloudflare。

账号：`Xinglin-Hu`  
网站仓库：`xinglin-hu.github.io`  
发布成功后的地址：<https://xinglin-hu.github.io/>

## 1. 先检查是否已有网站仓库

登录 GitHub，然后打开 [目标仓库](https://github.com/Xinglin-Hu/xinglin-hu.github.io)。

- 如果能看到仓库，先检查已有文件和 Settings → Pages。已有网站内容不要直接覆盖，先确认要保留什么。
- 如果确认这个账号没有该仓库，再进行下一步。未登录时显示 404 也可能只是私有仓库不可见，不能仅凭这个判断仓库不存在。

## 2. 创建仓库

打开 [新建仓库页面](https://github.com/new)，填写：

| 设置 | 选择／填写 |
|---|---|
| Owner | `Xinglin-Hu` |
| Repository name | `xinglin-hu.github.io` |
| Description | `Personal academic website of Xinglin Hu` |
| Visibility | **Public** |
| Add README | 开启 |
| Add .gitignore | 不添加 |
| Choose a license | 暂时不添加 |

点击 **Create repository**。仓库名按官方用户站规则使用小写。免费 GitHub 套餐支持从公开仓库发布 Pages；私有仓库需要支持此功能的付费套餐。[GitHub 官方建站说明](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

## 3. 解压网站包并上传

下载提供的网站 ZIP 包，在 Windows 文件资源管理器中右键 → **全部解压缩**。

进入解压后的文件夹，找到能直接看到 `index.html`、`_config.yml`、`_data`、`assets` 和 `files` 的那一层。回到 GitHub 仓库的 **Code** 页面，点击 **Add file → Upload files**，把这一层里的所有文件和文件夹一起拖入上传区域。

**上传的是解压后的内容，不是 ZIP，也不是包住这些内容的外层文件夹。** GitHub 不会自动解压 ZIP。正确上传后，仓库顶层应有这样的结构：

```text
xinglin-hu.github.io/
├── _config.yml
├── index.html
├── 404.html
├── README.md
├── _data/
│   ├── profile.yml
│   ├── publications.yml
│   ├── experience.yml
│   ├── education.yml
│   ├── projects.yml
│   └── awards.yml
├── assets/
│   ├── style.css
│   └── favicon.svg
└── files/
    └── cv.pdf
```

等待上传完成。在提交说明中填写 `Add personal website`，选择 **Commit directly to the main branch**，点击 **Commit changes**。这一操作把文件保存到网站使用的主分支。新建仓库自动生成的 `README.md` 可由网站包提供的版本替换。

GitHub 支持在浏览器中拖入文件夹；目前每次最多上传 100 个文件，每个文件上限为 25 MiB。本包的日常维护可以通过网页完成。[GitHub 网页上传说明](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)

## 4. 开启网站发布

打开仓库顶部的 **Settings**，在左侧选择 **Pages**。在 **Build and deployment** 区域设置：

| 设置 | 选择 |
|---|---|
| Source | **Deploy from a branch** |
| Branch | **main** |
| Folder | **/ (root)** |

点击 **Save**。`Custom domain` 暂时留空。你使用的是免费的 GitHub 地址，不需要购买域名。[GitHub 发布来源设置说明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

初次发布可能需要几分钟；GitHub 说明更改可能需要最多约 10 分钟才出现在网站上。可以打开仓库 **Actions**，查看最新的 Pages 构建是否成功；然后回到 **Settings → Pages**，使用 **Visit site** 访问。[GitHub Pages 快速入门](https://docs.github.com/en/pages/quickstart)

## 5. 上线后检查

打开 <https://xinglin-hu.github.io/>，检查：

- 首页姓名、研究简介和公开邮箱是否正确。
- 论文标题、作者、年份及录用／在投等状态是否准确。
- CV 按钮能否打开原版 `cv.pdf`。
- 邮箱和 GitHub 链接是否正常。
- 手机屏幕上文字是否清楚、导航是否可用。

本版按你的要求保留原版 CV 下载，原文件中的内容也会随之公开。没有提供或核实的论文、代码、Google Scholar 地址不应补造；以后有真实链接时再加入。

## 6. 以后在哪里修改内容

日常主要编辑 `_data` 文件夹中的文字，不需要改页面布局：

| 想更新什么 | 打开的文件 |
|---|---|
| 简介、邮箱、身份、个人链接 | `_data/profile.yml` |
| 论文、作者、发表状态和论文链接 | `_data/publications.yml` |
| 研究经历与实习 | `_data/experience.yml` |
| 教育经历 | `_data/education.yml` |
| 项目与论文研讨会 | `_data/projects.yml` |
| 奖项与荣誉 | `_data/awards.yml` |
| 下载的简历 | `files/cv.pdf` |
| 网站标题、描述、正式网址 | `_config.yml` |
| 页面结构／栏目 | `index.html` |
| 颜色、字号、间距等外观 | `assets/style.css` |

具体操作：打开文件 → 点击右上角铅笔 **Edit this file** → 修改 → **Commit changes…** → 填写简短说明 → 选择直接提交到 `main` → **Commit changes**。等构建完成后刷新网站。[GitHub 网页编辑说明](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)

这些 `.yml` 文件通过缩进表达结构。修改时保留已有的英文键名、冒号、引号和缩进；新增论文或经历时，复制一整项后替换内容最方便。使用空格，不要用 Tab 缩进。只写已经核实的论文状态和链接。

同一项研究只列一次。若同一论文在不同投稿或会议中使用了不同题目，在这条论文的 `versions` 中补充题目、会议和状态。本版已把 ORGEval 与 ICML CTB Workshop 的题目合并展示；没有其他版本时保留 `versions: []`。

更新简历时，先将新 PDF 命名为 `cv.pdf`，在 GitHub 打开 `files` 文件夹，再选择 **Add file → Upload files**，上传并提交同名文件。这样网站中的 CV 地址可以继续使用。若不保留文件名，需要同步修改引用它的链接。

## 常见问题

| 现象 | 优先检查 |
|---|---|
| 网站显示 404 | 是否已经发布成功；仓库名称是否正确；Pages 是否选择 `main` 和 `/ (root)` |
| 首页显示 README | `index.html` 是否在仓库顶层，而不是嵌在解压包的外层文件夹中 |
| 页面显示模板代码或缺少数据 | 是否误加了 `.nojekyll`；本站需要 GitHub 的 Jekyll 构建，请保留 `_data` 和 `_config.yml` |
| 更新后还是旧内容 | Actions 中最新发布是否完成；完成后用无痕窗口重新打开 |
| Actions 出现红叉 | 先打开失败记录；最近修改的数据文件是否破坏了引号、冒号或缩进 |
| CV 无法打开 | 是否存在 `files/cv.pdf`，文件名大小写是否一致，是否意外上传成 ZIP |
| 上传页显示新分支／Propose changes | 查看是否选成了新分支；内容必须进入 Pages 使用的 `main` 分支才会发布 |

本站依赖 GitHub 默认的 Jekyll 构建，因此不要额外添加 `.nojekyll`；也不需要新增 Astro、Node 或自定义工作流。[GitHub Pages 与 Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)

步骤核对日期：2026-09-26。界面文字以后可能略有调整，设置含义保持以 GitHub 官方说明为准。
