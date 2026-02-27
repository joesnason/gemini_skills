# Super Extension (gemini_skills)

[![Version](https://img.shields.io/badge/version-1.1.0-blue.svg)](gemini-extension.json)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

這是一個為 Gemini CLI 設計的全能擴充套件，旨在提升開發效率，涵蓋了 Build 分析、Git 流程自動化以及商務郵件撰寫三大核心功能。

## 🚀 核心功能

### 1. 🛠️ Build 分析 (`analyze-build`)
自動掃描並分析 `logs/` 目錄下的建置日誌。
- **錯誤定位**：精確識別 Jenkins、Ninja、Make 或編譯錯誤。
- **修復建議**：根據 `internal-wiki.md` 中的知識庫提供具體的解決方案。
- **智能過濾**：區分 Warning 與 Error，專注於解決致命阻礙。

### 2. 📝 Git 提交與推送 (`commit-push`)
簡化 Git 工作流，確保 Commit 訊息專業且符合規範。
- **自動摘要**：分析變更內容並生成專業的 Commit Message。
- **一鍵操作**：自動執行 `git status`、`git add`、`git commit` 並 `git push origin main`。

### 3. 📧 商務郵件助理 (`mail-creator`)
將簡短的筆記或重點轉化為專業的商務英文郵件。
- **語氣優化**：確保郵件禮貌且符合企業形象。
- **快速生成**：只需提供關鍵資訊，即可生成完整的郵件草稿。

## 📂 專案結構

```text
.
├── gemini-extension.json    # 擴充套件定義與配置
├── internal-wiki.md        # Build 錯誤模式與分析知識庫
├── README.md               # 本文件
└── commands/               # 指令定義檔
    ├── analyze-build.toml
    ├── commit-push.toml
    └── mail-creator.toml
```

## 🛠️ 安裝與使用

1. **配置**：確保 `gemini-extension.json` 已正確載入至您的 Gemini CLI 環境。
2. **知識庫**：分析功能依賴於 `internal-wiki.md`，建議根據團隊需求持續更新此檔案。

### 常用指令

- **執行 Build 分析**：
  使用 `analyze-build` 指令來檢查最近的失敗日誌。
- **提交代碼**：
  完成開發後，直接調用 `commit-push` 完成後續流程。
- **撰寫郵件**：
  提供郵件重點，交由 `mail-creator` 進行潤飾。

## 📖 內部 Wiki 摘要

專案包含一份 `internal-wiki.md`，記載了常見的 Jenkins 錯誤模式（如 `hudson.AbortException`, `Timeout exceeded` 等）以及 Ninja/Make 的分析技巧。這份文檔是 `analyze-build` 指令的核心上下文。

---
**版本**: 1.1.0 | **作者**: jonathan Hsieh | **授權**: MIT
