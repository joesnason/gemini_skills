# Gemini Skills

此專案收集了一系列實用的 Gemini CLI 指令，幫助開發者自動化日常開發流程，包含 Build 分析、Git 提交流程以及商務郵件撰寫。

## 安裝方式

使用以下指令安裝此擴充功能：

```bash
gemini extensions install https://github.com/joesnason/gemini_skills
```

## 反安裝方式

若要移除此擴充功能，請使用以下指令：

```bash
gemini extensions uninstall gemini_skills
```

## 指令使用方式

安裝完成後，您可以在 Gemini CLI 中直接呼叫以下指令：

### 1. `/analyze-build`
自動分析 `logs/` 資料夾中的 build log，定位錯誤原因並提供修復建議。
- **功能**：搜尋關鍵字（如 `error`、`FAILED`）、識別失敗階段、提供根因分析。
- **輸出**：產生 `build-break-report.md` 包含分析摘要、錯誤列表與修復建議。

### 2. `/commit-push`
自動化 Git 提交與推送流程。
- **功能**：執行 `git status` 與 `git diff`，自動撰寫專業的 Commit Message，並執行 `commit` 與 `push` 到遠端倉庫。

### 3. `/mail-creator`
將簡短的筆記、草稿或碎碎念轉換為專業、禮貌且簡潔的商務英文郵件。
- **功能**：優化語氣、確保商務專業形象，適合處理回覆信件或正式通知。
- **使用**：可搭配 `stdin` 傳入內容。
