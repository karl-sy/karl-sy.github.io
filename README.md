# 原能矩阵 · 老回忆 官网

杭州原能矩阵技术有限公司官方网站 —— 为老年人留存一生的故事。

## 目录结构

```
website/
├── index.html      # 首页：定位 + 核心服务 + 服务对象 + 承诺
├── about.html      # 关于我们：公司简介、使命、原则
├── service.html    # 服务流程：七步成书 + 常见疑问
├── contact.html    # 联系我们
├── css/main.css    # 全站样式（响应式，移动端适配）
└── images/         # 图片资源（hero、family 配图）
```

## 本地预览

直接用浏览器打开 `index.html`，或启动本地服务器：

```bash
cd website
python3 -m http.server 8000
# 访问 http://localhost:8000
```

## 零成本部署（Cloudflare Pages）

1. 在 GitHub 创建公开仓库，推送 `website/` 目录下所有文件
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com) → Workers & Pages → Create → Pages → Connect to Git
3. 选择该仓库，构建命令留空，输出目录填 `/`（或仓库根目录即 website 内容）
4. 部署完成后获得免费域名：`https://<项目名>.pages.dev`

### 替代方案：GitHub Pages

1. 推送仓库后，Settings → Pages → Source 选 `main` 分支
2. 访问 `https://<用户名>.github.io/<仓库名>/`

## 后续可升级

- 自定义域名（约 ¥70/年，`.com`/`.cn`）→ CNAME 指向 Pages，免费 HTTPS
- 咨询表单 → Cloudflare Workers 免费额度（10 万次请求/天）
- 真实案例展示 → 替换 `index.html` 服务对象区块
- 联系方式 → `contact.html` 中的邮箱与电话，请按需核对更新
