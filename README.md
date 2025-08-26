# 用 VS Code + GitHub 同步写小说（简明版）

## 0. 准备

- 电脑装好 Git（装完在终端跑 git --version）。

- 注册 GitHub 账号并登录。

- 装 VS Code，点击左侧 Source Control（源代码管理） 图标能看到 Git 面板。

- 可选扩展（极简三件套）：

-- Markdown All in One（舒适写作）

-- Git Graph（看提交历史更直观）

-- Paste Image（粘贴截图自动存入 images/）

## 1. 拉取仓库（只做一次）

- A. 在 GitHub 网页上找到

- 点 “Code” → 复制 HTTPS 地址（如 <https://github.com/you/novel-moonriver.git）。>

- B. 在 VS Code 打开并克隆

- VS Code：Ctrl/Cmd+Shift+P → Git: Clone → 粘贴仓库地址 → 选择本地文件夹 → 打开。

## 2.基础结构

/novel
/chapters # 正式章节
/drafts # 草稿
/outline # 大纲与人物设定
/images # 插图（尽量小于 10MB）
README.md # 项目说明
.gitignore

## 3.提交并首次推送

VS Code 左侧 Source Control(源代码管理)：

全选变更 → +（Stage 暂存）→ 填信息：（做了什么内容） → 提交（Commit）

点 Sync / Push 同步到 GitHub。

## 日常写作（4 步循环）

- 口诀：先拉再写，多存勤推。

- Pull：打开 VS Code，左下角 “↓” 或 Git: Pull

- 写：在 chapters/ 新建 ch01-初遇.md，边写边 Ctrl/Cmd+S 保存。

- Commit：Source Control → 选中变更 → 填信息（例如 ch1: 初遇场景成稿）→ 提交。

- Push：点 “↑” 或 Sync 推送到 GitHub（远端=你的云备份）。

---

小建议：每写完一个“自然段落/情节节点”就提交一次，崩溃也不怕。'

## ps. 多人协作（最简安全流）

一句话：分支写 → 提 PR → 代码审阅 → 合并。

- 创建分支：VS Code 左下角分支名 → Create New Branch，命名如 feat/chapter-02。

- 在分支上写，像平时一样 Commit & Push。

- GitHub 开 PR：网页点 “Compare & pull request”，标题如 feat: chapter 02 初稿。

- 对方 Review：评论/修改后点击 Merge。

- 本地切回 main：Git: Checkout to... → main，再 Pull 同步。

单人写也可以一直在 main 上写；两人以上请用分支 + PR，冲突更少。
