# sync-value-web

シンクバリュー株式会社（Syncvalue Inc.）公式コーポレートサイト。

- 静态三页站，纯 HTML/CSS，无构建步骤：`index.html`（首页）、`business.html`（事業紹介）、`privacy.html`（隐私政策）。`.nojekyll` 关闭 Jekyll 处理。
- 部署：GitHub Pages，自定义域名 `sync-value.com`（见 `CNAME`）。
- 这是 **sync-value 经营中枢（hub）的网站 spoke**——技术实现独立于 hub 仓库（见 hub 项目 ADR-0001 / 支线登记表）。

## 本地预览

直接用浏览器打开 `index.html` / `business.html` / `privacy.html` 即可。

## 部署（GitHub Pages）

1. push 到 `ohlasermiao/sync-value-web`（public）。
2. Settings → Pages → Source 选 `main` 分支根目录。
3. 自定义域名由 `CNAME` 文件（`sync-value.com`）自动识别；在 onamae.com 加 A 记录指向 GitHub Pages IP。
4. 勾选 Enforce HTTPS（证书自动签发）。
5. **内链一律用无后缀 URL**（如 `/business` 而非 `/business.html`）——GitHub Pages 会对带 `.html` 的链接做 308 跳转，新增页面/改链接时照此约定，避免每次点击多一次跳转（见 2026-06-13 commit）。
