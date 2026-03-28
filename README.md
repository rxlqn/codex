# 跨时区会议时间协调器

这是一个静态网页工具，帮助你输入多个地区/时区后：

- 找到大家**工作时间重叠**的会议窗口；
- 如果没有重叠，给出一个尽量让大家都清醒、且尽可能友好的开会时间。
- 页面中的“重叠时间”和“建议会议时间”默认使用**中国时间（UTC+8）**显示。

## 本地打开

直接双击 `index.html` 即可使用。

## GitHub Pages 部署

仓库已包含自动部署工作流：`.github/workflows/deploy-pages.yml`。

### 1) 推送到 GitHub

把当前仓库推送到你自己的 GitHub 仓库（例如 `https://github.com/<user>/<repo>`）。

### 2) 开启 Pages

在仓库设置：

- `Settings` → `Pages`
- `Build and deployment` 选择 `GitHub Actions`

### 3) 等待部署完成

推送后会自动触发 `Deploy static site to GitHub Pages`。

部署完成后的测试链接格式为：

- `https://<user>.github.io/<repo>/`

例如仓库是 `https://github.com/alice/time-overlap-planner`，则链接是：

- `https://alice.github.io/time-overlap-planner/`

## 如果部署失败（常见修复）

1. 确认仓库 **Settings → Pages** 中 Source 已选 `GitHub Actions`。
2. 确认 Actions 权限允许创建和部署 Pages（`Settings → Actions → General`）。
3. 确认默认分支里存在 `index.html`（本仓库工作流会复制到 `_site/index.html` 再部署）。
4. 若你是 Fork 仓库，请确认仓库未禁用 Pages 功能。
