# THEOS Jarvis UI

> THEOS 生態系的 AI 助理與研發工作介面。以模組化、可追溯、安全優先為原則，逐步整合知識、工程資料、AI Agent、專案工作流與 Digital Twin。

## 專案簡介

THEOS Jarvis UI 是 THEOS / TKOS 的使用者介面與工作入口，目標是將知識、工程工具與 AI 工作流程整合成一致、可擴充的操作體驗。

本 Repository 目前處於初始化階段。本文件描述專案願景與建議架構；除非有實際程式碼、測試或執行證據，否則不將規劃中的能力視為已完成。

## 設計原則

- **SSOT（Single Source of Truth）**：重要設定、介面契約與文件具有明確且可追蹤的來源。
- **模組化**：功能可獨立開發、測試、替換及擴充。
- **文件先行**：先更新需求、架構與驗收條件，再實作功能。
- **安全優先**：採用最小權限原則；機密、Token 與密碼不得提交至 Repository。
- **可追溯性**：重要操作、資料來源、版本與錯誤應能追查。
- **漸進式驗證**：先建立可執行的最小版本，再逐步擴充。
- **供應商可替換**：AI 與外部服務透過 Adapter / API 契約整合，避免核心程式碼被單一服務綁定。

## 專案目標

1. 建立一致、清晰、可擴充的 Jarvis UI。
2. 提供 AI 對話、任務工作區與專案狀態檢視。
3. 預留 THEOS / TKOS 知識庫、工程資料庫及模組庫的整合介面。
4. 預留工具連接、任務流程、權限管理與執行紀錄的呈現能力。
5. 為後續 Agentic AI、Digital Twin 與 Runtime 整合建立穩定的 UI 邊界。

## 初始架構

```
THEOS Jarvis UI
├── Presentation Layer
│   ├── Dashboard / Workspace
│   ├── AI Conversation
│   ├── Project & Task Views
│   └── Settings / Connection Status
├── Application Layer
│   ├── Session & State Management
│   ├── Task Workflow
│   └── Permission / Error Handling
├── Integration Layer
│   ├── AI Provider Adapter
│   ├── THEOS / TKOS Knowledge Adapter
│   ├── Repository / Engineering Data Adapter
│   └── Runtime / Digital Twin Adapter（未來整合）
└── Foundation
    ├── Configuration
    ├── Logging & Diagnostics
    ├── Security Boundaries
    └── Tests & Documentation
```

> ⚠️ 以上是待驗證的設計方向，不代表這些模組已經實作。技術堆疊、目錄結構與 API 契約應在第一個可執行版本建立時確認並記錄。

## 開發路線圖

### Phase 0 — Bootstrap

- [ ] 建立 Repository 基礎文件與目錄結構
- [ ] 確認產品需求、使用情境與 MVP 範圍
- [ ] 決定前端技術堆疊、套件管理工具與執行環境
- [ ] 建立版本控制、基本檢查與安全規範

### Phase 1 — UI MVP

- [ ] 建立可啟動的應用程式骨架
- [ ] 建立主畫面與導覽
- [ ] 建立 AI 對話介面與載入、錯誤、空狀態
- [ ] 建立設定頁與連線狀態呈現
- [ ] 加入基本測試與使用說明

### Phase 2 — THEOS / TKOS Integration

- [ ] 定義知識物件與工程資料的介面契約
- [ ] 整合知識查詢與專案資料檢視
- [ ] 加入任務、模組及文件關聯導覽
- [ ] 加入可追溯的操作與錯誤紀錄

### Phase 3 — Agent & Runtime

- [ ] 定義 Agent 工具權限與執行邊界
- [ ] 建立任務狀態、審核與中止流程
- [ ] 評估 Digital Twin / Runtime 整合需求
- [ ] 建立整合測試、安全測試與版本發布流程

## 安全規範

- ❌ 不得提交 API Key、Access Token、密碼、私鑰或個人機密資料。
- ✅ 使用環境變數或適當的 Secret 管理機制保存敏感設定。
- ✅ 外部工具與 Agent 動作應採最小權限，並在需要時要求使用者確認。
- ✅ 對外部輸入、檔案與工具輸出進行驗證，不將其直接視為可信指令。
- ✅ 變更權限、部署或刪除資料等高影響操作，應具備明確的授權與錯誤處理。

## 開發與執行

目前尚未確定技術堆疊，因此暫不提供可能不適用的安裝或啟動指令。待前端框架、套件管理工具及專案骨架確立後，應在本節補上：

- 環境需求與版本
- 安裝依賴
- 本機開發啟動方式
- 測試、Lint 與 Build 指令
- 環境變數設定範例
- 部署與故障排除方式

## 文件與變更規範

每次新增功能或修改既有行為，應依序完成：

1. 更新需求與設計文件。
2. 定義介面、資料格式及驗收條件。
3. 實作功能並補上測試。
4. 執行相關檢查並記錄結果。
5. 更新 README、變更紀錄與使用方式。

## 貢獻與問題回報

提交變更前，請確認變更範圍清楚、文件同步更新，並通過適用的測試與檢查。

回報問題時，請提供：
- 重現步驟
- 預期行為
- 實際行為
- 相關錯誤訊息

> ⚠️ 請勿附上 Token 或其他機密資料。

## 授權

尚未指定。正式對外發布或接受外部貢獻前，請確認專案授權方式，並新增相應的 LICENSE 檔案。

## 專案連結

- 📍 GitHub Repository: [Danzexu26-sng/theos-jarvis-ui](https://github.com/Danzexu26-sng/theos-jarvis-ui)

---

**最後更新**：2026-10-10
