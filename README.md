# rillo 网站

rillo.dev 的占位页与站点文档页（条款 / 隐私）。纯静态，无构建：`index.html`、`terms.html`、`privacy.html` + `site.css` + `favicon.svg`。

本地预览：

```bash
python3 -m http.server 4173
```

部署：GitHub Pages，legacy 构建，`main` 分支根目录。站点 https://rillo.dev/ ，自定义域名由 `CNAME` 声明。

DNS 在 Dynadot（Dynadot DNS 模式）：

- `@` A → `185.199.108.153`、`185.199.109.153`、`185.199.110.153`、`185.199.111.153`
- `@` AAAA → `2606:50c0:8000::153`、`2606:50c0:8001::153`、`2606:50c0:8002::153`、`2606:50c0:8003::153`（可选）
- `www` CNAME → `ysheep666.github.io`

证书签发后在仓库 Settings → Pages 勾选 Enforce HTTPS。本机 DNS 走代理 fake-ip 时 `dig` 会看到 `198.18.x.x`，用 dnschecker.org 或 DoH 验证真实解析。
