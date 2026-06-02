# sync-value-web

シンクバリュー株式会社（Syncvalue Inc.）公式コーポレートサイト。

- 静态单页，纯 HTML/CSS（`index.html`），无构建步骤。
- 部署：GitHub Pages，自定义域名 `sync-value.com`（见 `CNAME`）。
- 这是 **sync-value 经营中枢（hub）的网站 spoke**——技术实现独立于 hub 仓库（见 hub 项目 ADR-0001 / 支线登记表）。

## 本地预览

直接用浏览器打开 `index.html` 即可。

## 部署（GitHub Pages）

1. push 到 `ohlasermiao/sync-value-web`（public）。
2. Settings → Pages → Source 选 `main` 分支根目录。
3. 自定义域名由 `CNAME` 文件（`sync-value.com`）自动识别；在 onamae.com 加 A 记录指向 GitHub Pages IP。
4. 勾选 Enforce HTTPS（证书自动签发）。
