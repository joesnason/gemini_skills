# Jenkins & Build 分析知識庫

## Jenkins 特定錯誤模式

- **"Build failed in stage"**: Pipeline stage 失敗。
- **"script returned exit code"**: Shell 腳本執行錯誤。
- **"hudson.AbortException"**: Jenkins 中斷異常。
- **"java.io.IOException"**: 系統 IO 錯誤。
- **"Timeout exceeded"**: 任務執行超時。
- **"No space left on device"**: 磁碟空間不足。
- **"Permission denied"**: 權限問題。
- **"Could not resolve dependencies"**: 依賴包解析或下載失敗。
- **"Compilation failure"**: 程式碼編譯失敗。

## 分析注意事項

- **區分層級**: 仔細區分 Warning 與 Error，專注於導致中斷的致命錯誤。
- **編譯細節**: 編譯錯誤通常伴隨檔案路徑與行號，請精確定位。
- **Ninja/Make**: Ninja 失敗通常會顯示具體缺少的標的 (target) 或檔案。
- **Pipeline 脈絡**: 識別失敗發生的具體 Stage 名稱。
- **大檔案處理**: Log 檔案較大時，優先使用搜尋功能搜尋關鍵字而非全文讀取。

## 指令使用說明

### 1. Build 分析 (`analyze-build`)
- **功能**: 自動檢查 `logs/` 下的日誌，定位錯誤並提供修復建議。
- **使用時機**: 當 Jenkins 或本地 Build 失敗時使用。

### 2. Git 提交與推送 (`commit-push`)
- **功能**: 自動檢查 Git 狀態，產生專業的 Commit Message 並推送到遠端倉庫。
- **流程**:
    1. 確認 `git status`。
    2. 自動撰寫 Commit Message。
    3. 執行 `git commit`。
    4. 推送至 `origin main`。

### 3. 商務郵件助理 (`mail-creator`)
- **功能**: 將草稿、碎碎念或簡單筆記轉換為專業、禮貌的商務英文郵件。
- **使用時機**: 需要撰寫正式對外或公司內部郵件，但只有簡短重點時。
- **特點**: 確保語氣符合企業形象，優化表達方式。
