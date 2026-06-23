# AppSource 公開文件站（GitHub Pages）

> **公開網址**：https://taipei-fishery.github.io/taiwan-vibe-coding-docs/  
> **原始碼 repo**：`taipei-fishery/taiwan-vibe-coding-docs`（public）  
> **編輯來源**：本 monorepo 的 `docs-site/`（private `taipei-seafood`）

主 monorepo 為 **private**，AppSource 法律／說明 URL 須指向此 **public** Pages 站，勿使用 `github.com/.../blob/main/...`。

## 同步到 public repo

```bash
# 自 monorepo 根目錄
./scripts/sync_appsource_docs.sh
```

腳本會將 `docs-site/`（含 Pages workflow）推送到 `taiwan-vibe-coding-docs`。

## app.json 對應 URL

| 欄位 | URL |
|------|-----|
| privacyStatement | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/privacy.html |
| EULA | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/eula.html |
| help（P2） | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/help/payroll.html |
| help（P2 操作） | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/help/payroll-operations.html |
| help（P4） | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/help/einvoice.html |
| help（P4 操作） | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/help/einvoice-operations.html |
| 入門指南 | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/getting-started.html |
| url | https://taipei-fishery.github.io/taiwan-vibe-coding-docs/ |

## 首次啟用 Pages

1. GitHub → `taiwan-vibe-coding-docs` → **Settings** → **Pages**
2. **Build and deployment** → Source：**GitHub Actions**
3. push 後 `Deploy GitHub Pages` workflow 會自動發佈

## 之後換自訂網域

於 Pages 設定 CNAME（例如 `docs.taiwan-vibe-coding.com`），並更新 `products/tw-payroll-bc/app.json`、`tw-einvoice-bc/app.json` 四個 URL 前綴即可。
