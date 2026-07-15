# AB-731 示範環境（Demo Environment）

> 本文件僅供講師使用（trainer-only），**請勿**發給學員。學員面向內容請見 `../README.md`；
> 授課節奏與 Demo 對應請見 [`teaching-guide.md`](teaching-guide.md)。

## 1. 目的與範圍

AB-731 是**商業領導者、無程式碼**課程，因此**沒有學員動手做的 Azure/Skillable Lab**。
講師的示範以 **Microsoft 365 Copilot**（SaaS，租戶層級）為主，用真實感的商業情境展示
「Copilot 如何在會議與日常工作流程中創造價值」。

現成的示範資產放在 **`../DEMO/20260415-Inventec/`**，以一家虛構的 ODM 製造商（英業達 / Inventec）
為情境包裝，涵蓋三個貼近製造業的場景。

### Terraform 為何 N/A
course-prep 技能中的 Terraform 是「講師示範用的後備資源堆疊」。但本課的示範全部落在
**Microsoft 365 Copilot 的 SaaS 體驗**（Teams/Word/Excel/Outlook/PowerPoint/Planner），
**不需要佈建任何 Azure 資源**（無 Foundry 專案、無金鑰、無運算資源）。因此本課
**不提供 Terraform 堆疊**；示範環境的準備是**手動的租戶／授權設定**（見第 5 節）。

## 2. 產品涵蓋範圍與缺口（重要）

| 課程主題 | Demo 是否涵蓋 | 說明 |
|---|---|---|
| Microsoft 365 Copilot（Chat / Teams / Word / Excel / Outlook / PowerPoint / Planner） | ✅ 充分 | 三個場景的核心 |
| Copilot 會議全流程（會前／會中／會後、Facilitator、AI Summary、Channel Agent） | ✅ 充分 | 場景一/二/三皆有 |
| Copilot Cowork（Frontier） | ◐ 部分 | 僅場景三 Demo 4 帶到端到端自動化 |
| **Copilot Studio（打造／客製 agent）** | ❌ 未涵蓋 | 課程 B1 有教，但 Demo 無實作 |
| **Microsoft Foundry / Azure AI（Vision/Language/Doc Intelligence/Search）** | ❌ 未涵蓋 | 課程 B2 / C1 有教，但 Demo 無實作 |
| 負責任 AI 治理實作（C3） | ❌ 未涵蓋 | 概念課，Demo 僅口頭帶到 |

> ⚠️ **缺口提醒**：若學員特別想看 **Copilot Studio 建 agent** 或 **Foundry** 的實際畫面，
> 現成 Demo 資產無法滿足，請改用官方影片或 `../README.md` 連結中的產品文件輔助說明，
> 並在課後誠實告知這部分為概念講授。

## 3. 資產清單（`../DEMO/20260415-Inventec/`）

**Demo 腳本（Markdown，講師逐步操作用）**
- `Teams會議全流程_會前會中會後_Demo步驟.docx.md` — 跨場景通用的會議生命週期主線
- `場景一_NPI新產品導入_Demo步驟.docx.md`
- `場景二_供應鏈風險管理_Demo步驟.docx.md`
- `場景三_QBR季度業務回顧_Demo步驟.docx.md`

**範例資料檔（上傳到示範租戶用）**
- Word：`英業達_NPI_Kickoff_會議逐字稿`、`英業達_NPI_設計審查會議逐字稿`、`英業達_NPI週報範本`、
  `英業達_供應商往來郵件串`、`英業達_供應鏈風險分析報告`、`英業達_供應鏈風險會議逐字稿`、
  `英業達_QBR準備郵件串`、`英業達_QBR預演會議逐字稿`、`英業達_會議總結範本`
- Excel：`英業達_BOM成本分析`、`英業達_ERP原始出貨記錄`、`英業達_NPI_ProServerX200_專案追蹤`、
  `英業達_PO採購訂單追蹤`、`英業達_QBR_KPI_Dashboard`、`英業達_供應商評估表`

**產生器（Python，僅供重建資料，不需在課堂使用）**
- `create_excel_files.py`、`create_supplementary_excel.py`、`create_word_files.py`、
  `create_meeting_template.py`、`create_qbr_meeting.py`、`create_scm_meeting.py`
- 這些腳本會產生上述 `.docx` / `.xlsx`。若要調整情境數據，改腳本後重跑即可。

## 4. 場景地圖

| 場景 | 情境主軸 | 主要 Demo | 建議時間 |
|---|---|---|---|
| **一 · NPI 新產品導入** | ProServer X200 AI 推論伺服器開發 | Teams Facilitator（即時協作）、Teams Notes + AI Summary（會後多角度摘要）、Copilot Chat 跨頻道彙整、Channel Agent、Word 週報自動產生 | 約 80–90 min |
| **二 · 供應鏈風險管理** | GPU Module 斷供危機與替代料評估 | 供應鏈風險會議全流程、Outlook 供應商溝通、Excel 供應商評估與成本分析、PowerPoint 管理層簡報、Word 風險分析報告 | 約 100–120 min |
| **三 · QBR 季度業務回顧** | Dell 2025 年度 QBR 準備與執行 | QBR 預演會議全流程、**Copilot Cowork** 端到端工作流程、Outlook、Excel KPI Dashboard、PowerPoint 客戶簡報 | 約 90–110 min |

- 每個場景都附「加碼實戰情境」與「學員練習建議」，可依產業與時間彈性抽取。
- **建議**：依學員產業選 **1 個場景**深入，其餘用「串接總結」帶過，避免時間超支。

## 5. 開課前設定（手動）

1. **租戶與授權**：示範帳號需具備 **Microsoft 365 Copilot** 授權（含 Teams、Word、Excel、
   Outlook、PowerPoint）。若要示範場景三 Demo 4，需可用 **Copilot Cowork**。
2. **上傳範例資料**：把第 3 節的 `.docx` / `.xlsx` 上傳到示範帳號的 OneDrive/SharePoint，並在
   Teams 建立對應頻道（例如 `#NPI-ProServerX200`），讓 Copilot 的跨 App 搜尋有資料可抓。
3. **索引時間**：資料上傳後，Copilot/Graph 需要時間建索引；**請提前一天**準備，避免當天搜不到。
4. **逐字稿**：會議逐字稿為模擬檔，可直接貼進 Teams/Word 作為「會議轉錄」的替身。
5. 依 [`teaching-guide.md`](teaching-guide.md) 第 7 節的 Preflight 清單逐項確認。

## 6. 備援方案（現場連線失敗時）

- 事先**預錄**每個核心 Demo 的畫面，或準備關鍵步驟**截圖**。
- 保留一份「Copilot 回應範例」文字，萬一即時產生結果不如預期，可展示預期輸出並說明。
- 網路不穩時，優先示範**會後摘要**與**Word/Excel 內嵌 Copilot**（比跨 App 搜尋穩定）。

## 7. 敏感性與授權（務必確認）

- **資料為虛構／模擬**：所有 `英業達_*` 檔案與逐字稿皆為**教學用模擬資料**，非真實客戶資料。
- **名稱使用**：場景以真實公司名稱（英業達 / Inventec，以及情境中提到的 Dell、HP、Broadcom 等）
  作為情境包裝。這些屬**講師內部素材**：
  - 對外交付、公開錄影或放上公開平台前，請**改為中性化名稱**（例如「某 ODM 廠」）或
    取得相關方授權。
  - 不要把模擬的財務數字、供應商評估、逐字稿當成任何公司的真實資訊引用。
- 本 `DEMO/` 目錄與範例檔屬 trainer-only；**不應**出現在學員面向的 `README.md` 中。

## 8. 關聯文件
- 學員面向課程參考：[`../README.md`](../README.md)
- 授課節奏與逐模組講點：[`teaching-guide.md`](teaching-guide.md)
