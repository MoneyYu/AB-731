# AB-731 備課指南（Teaching Guide）

> 課程 **AB-731T00-A：Drive AI transformation in your organization**（在組織中推動 AI 轉型）
> 對象：商業領導者（無需技術背景）｜長度：1 天｜完成方式：**Achievement Code**
> 相關認證：**Microsoft Certified: AI Transformation Leader**（考試 **AB-731**）
> 本文件僅供講師備課使用（trainer-only），**請勿**發給學員；學員面向內容請見 `../README.md`。

---

## 1. 課程定位與講授心法

- 這是一門**策略型、非技術**課程。學員是決策者，不是工程師。講授時聚焦「**為什麼、何時、投資報酬**」，而非「怎麼寫程式」。
- 每個技術名詞都要能翻成一句**商業語言**：例如 *grounding* →「讓 AI 只根據公司權威資料回答，降低亂編風險」。
- 全課貫穿三條主線，對應考試三大領域：
  1. **生成式 AI 的商業價值**（35–40%）
  2. **Microsoft AI 應用與服務的效益、能力與機會**（35–40%）
  3. **導入與採用策略**（20–25%）
- 投影片（`PPT/`，2025 年 12 月版）對應 Microsoft Learn 上的 **3 條學習路徑、8 個模組**。投影片與 Learn 內容一致；若日後 Learn 更新，以 Learn 為準（見第 6 節）。

### 投影片 ↔ 模組對應
| 投影片 | 學習路徑 | 模組 |
|---|---|---|
| `PowerPoint_Introduction` | — | 開場、Learn profile、Achievement Code、認證介紹 |
| `PowerPoint_01` | A 路徑 | A1 生成式 AI 基礎、A2 打造有效的生成式 AI 解決方案 |
| `PowerPoint_02` | B 路徑 | B1 Microsoft Copilot 解決方案、B2 Microsoft Foundry Tools |
| `PowerPoint_03` | C 路徑 | C1 善用 AI 工具、C2 創造商業價值、C3 負責任 AI、C4 規模化 AI |
| `PowerPoint_Conclusion` | — | 總結、下一步、認證行動呼籲 |

---

## 2. 建議議程（1 天）

> 依 `PowerPoint_Introduction` 投影片 6 與 Trainer Prep Guide（PDF）調整；下列為建議節奏。

| 時段 | 內容 | 時間 |
|---|---|---|
| 上午前段 | 開場 + 自我介紹 + 課程期待；**A1** 生成式 AI 基礎 | 90 min |
| 休息 | | 15 min |
| 上午後段 | **A2** 打造有效的生成式 AI 解決方案；A 路徑知識檢查與討論 | 75 min |
| 午餐 | | 60 min |
| 下午前段 | **B1** Copilot 解決方案（含 Teams 會議全流程 Demo 精簡版）；**B2** Foundry Tools | 100 min |
| 休息 | | 15 min |
| 下午後段 | **C1–C4** 轉型、五大準備度、負責任 AI、規模化；總結與認證行動 | 110 min |

- **互動時間**：每個模組保留 5–10 分鐘做投影片內的「Reflect and discuss」與 Knowledge check。
- Demo 建議安排在 B1（Copilot 實際運作最有感）；**課堂用 15–25 分鐘精簡版**，完整場景（80–120 分鐘）見 `demo-environment.md`，作為延伸或依產業選用。

---

## 3. 逐模組備課重點

> 每個模組列出：**目標一句話**、**關鍵講點**、**商業對照**、**易踩雷**。講點取自投影片講者備忘稿。

### A 路徑 — Explore the business value of generative AI solutions

#### A1 — Understand the foundations of generative AI for business leaders
- **目標**：讓學員能用商業語言解釋什麼是生成式 AI、能做什麼、成本與風險。
- **關鍵講點**：
  - AI＝模仿人類能力的軟體（視覺、語音、決策、擷取洞察）；**生成式 AI** 是其中「會產生內容」的子集（文字、圖像、程式碼）。
  - 資料科學 → 機器學習 → 深度學習的層次關係；Transformer 讓 LLM 具備語境理解。
  - **Microsoft 生成式 AI 版圖**：Microsoft 365 Copilot、Azure AI、GitHub Copilot、Dynamics 365 Copilot、Power Platform Copilot——各自的典型使用情境。
  - **Agents**：prebuilt（Copilot 內建）**vs** custom（Azure AI / Copilot Studio 客製）。
  - **模型類型與選擇**：LLM、程式碼模型、擴散（影像）模型、多模態、領域專用；選型準則＝效能、成本、隱私、整合、擴充性、治理。
  - **成本驅動**：Microsoft 365 Copilot＝可預測的訂閱、低導入門檻；Azure AI＝用量計費（token），隨規模成長。平均 ROI 約「投入 1 美元回收 3.7 美元」。
- **X vs Y 深入**：
  - **LLM vs SLM**：廣泛能力 vs 針對特定情境最佳化（成本／延遲更低）。
  - **Microsoft 365 Copilot（可預測）vs Azure AI（用量計費）**：turnkey、快速見效 vs 彈性、可控但複雜度高；多數組織**兩者並用**。
- **易踩雷**：學員常把「生成式 AI」當成「所有 AI」。強調 descriptive / predictive / prescriptive 也是 AI 價值來源。

#### A2 — Build effective generative AI solutions in your organization
- **目標**：理解讓 AI 可信、可靠的四件事：提示、接地、資料安全、機器學習。
- **關鍵講點**：
  - **Prompt engineering** 四要素：**Goal · Context · Source · Expectations**。用投影片 17 的三段式範例（逐步加上 Context、Source）展示提示品質如何改變輸出。
  - **Grounding / RAG**：把回答接到權威資料來源；用投影片 18 的 ISO 27001 新舊範例對比「未接地 vs 已接地」。RAG＝檢索→增強提示→生成。
  - **可信賴 AI**：資料品質（結構化／非結構化、乾淨、具代表性）＋安全（加密、驗證、治理）。
  - **機器學習價值與生命週期**：定義問題→蒐集／準備資料→訓練與驗證→部署→監控（MLOps）；領導者角色在**定義目標、配置資源、評估成果**。
- **易踩雷**：不要陷入 RAG 技術細節；重點是「為什麼商業上需要接地＝準確、合規、信任」。

**A 路徑 Knowledge check 解答（投影片 01/23）**
1. 接地於權威資料的關鍵好處？→ **提升準確性、合規與信任**。
2. RAG 的主要目的？→ **檢索並使用即時資料以產生準確回答**。
3. Microsoft app 內的 Copilot Agents 做什麼？→ **自動化如撰寫郵件、摘要會議等任務**。

---

### B 路徑 — Drive business value with AI solutions

#### B1 — Drive business value with Microsoft Copilot solutions
- **目標**：認識 Copilot 家族、如何對應到商業流程、如何導入與授權。
- **關鍵講點**：
  - **Copilot 是什麼**：跨 Microsoft 產品的 AI 協助，結合 LLM 與**組織資料**，內建於 Word/Excel/PowerPoint/Outlook/Teams。
  - 三大體驗：**Copilot Chat**（快速問答；**取用組織資料需 Microsoft 365 Copilot 授權**，否則預設為網路基礎）、**Microsoft 365 Copilot**（嵌入生產力 App）、**Copilot Studio**（低程式碼打造／客製 copilots 與 agents）。
  - 專業 agents：**Researcher**（彙整知識做報告）、**Analyst**（把資料變洞察）。
  - **對應商業流程**：文件密集（草擬政策／提案）、資料密集（預測／預算）、會議密集（策略會、專案更新）。從影響營收／合規／客戶體驗的流程切入 ROI 最高。
  - **Microsoft Graph**：把人、文件、對話、行事曆串起來，讓 Copilot 的回答有真實商業脈絡且遵守權限。
  - **授權**：隨 Microsoft 365 內含、月訂閱、隨用隨付；E3/E5/Business Standard/Premium 差異。**Copilot Studio 另計費**。
- **X vs Y 深入**：
  - **Copilot Chat vs Microsoft 365 Copilot vs Copilot Studio**：問答 vs App 內嵌 vs 打造／客製工具。可播放官方影片或自行解說。
  - **Buy vs Extend vs Build**：開箱即用 vs 用連接器擴充 vs 從零客製；對應速度、成本、彈性的策略取捨。
- **易踩雷**：學員常混淆 Copilot Studio 是不是「一種 agent」。澄清：它是**打造／客製 agents 的工具**，本身不是 agent。

#### B2 — Drive business value with AI using Microsoft Foundry Tools
- **目標**：知道 Foundry 是生成式 AI 與 agents 的**協調與治理層**，以及如何選模型與訂閱。
- **關鍵講點**：
  - Foundry 能力：探索與評估模型、管理安全與合規、監控效能、支援 agents 代為執行工作。
  - 核心 AI 能力對照商業：Generative AI、NLP、Computer Vision、Speech、Information Extraction、Decision Support。
  - Foundry 解決方案：Azure Vision、Azure Language、Azure Document Intelligence、Azure Search，由 Foundry 協調（如保險理賠情境串接多能力）。
  - **選模型**：Prebuilt（快、簡單）→ Foundry Models & RAG（彈性／創意）→ Fine-tuning & Custom（以企業資料求精準）。原則：**先簡單，商業理由夠強再加複雜度**。
  - **訂閱模式**：Pay-as-you-go（彈性、適合試點）vs Pre-paid（可預測、有折扣、適合成熟部署）。
- **X vs Y 深入**：**Prebuilt vs RAG vs Fine-tuning**；**Pay-as-you-go vs Pre-paid**。
- **易踩雷**：B2 出現最多技術名詞。時時拉回「這對決策者代表什麼投資／風險」。

**B 路徑 Knowledge check 解答（投影片 02/22）**
1. 最適合自動草擬政策文件並確保一致性的 Copilot？→ **Copilot in Word**。
2. Copilot Studio 的主要好處？→ **可為獨特商業需求打造與客製 copilots 與 agents**。
3. Azure Document Intelligence 在金融流程的關鍵優勢？→ **自動從文件擷取資料，降低人工與錯誤**。

---

### C 路徑 — Transform your business with AI

#### C1 — Leverage AI tools and resources for your business
- **目標**：認識 Microsoft 的 AI 策略框架與安全導入的分階段做法。
- **關鍵講點**：
  - **Microsoft AI 取徑 —「Becoming Frontier」**：成功框架四支柱（Enrich employee experiences、Reinvent customer engagement、Reshape business processes、Bend the curve on innovation）＋三大解決方案領域（**AI Business Solutions、Cloud & AI Platforms、Security**）。
  - Copilot 與 agents 三種工作轉變：加速個人生產力 → 改善流程 → 驅動功能性轉型（agents 端到端執行、人設目標與護欄）。
  - Azure 雲與 AI 平台：統一資料（Microsoft Fabric、Purview）、現代化（Migrate、Arc）、打造（Foundry、GitHub Copilot）。
  - **分階段安全導入：Govern → Secure → Manage**，對應 Microsoft **AI Adoption Framework（Cloud Adoption Framework）**。
- **易踩雷**：「Becoming Frontier」是願景框架，不是產品；別讓學員以為要「買 Frontier」。

#### C2 — Create business value with AI（五大 AI 準備度驅動因子）
- **目標**：用五大驅動因子把 AI 從實驗變成可靠的商業成果。
- **五大驅動因子**（投影片 11–16）：
  1. **Business strategy**：以結果排序使用情境；每個情境設 2–3 個 KPI；把 AI 當投資組合管理（投影片引用 Gartner：採用投資組合管理者更可能達成 AI 成熟度，約 2.4×；**此為課程講者稿引用的數據，對外沿用前請向 Gartner 原始報告查證**）。
  2. **Technology and data strategy**：架構對齊策略、準備資料estate、build vs buy。
  3. **AI strategy and experience**：小規模快速試點、量測要點、跨職能團隊。
  4. **Organization and culture**：由上而下領導、賦能多元團隊、投資學習。
  5. **AI governance**：統一治理模型（資料／AI／法規三支柱）、可操作並持續調整。
- **易踩雷**：學員愛談技術；提醒「文化與治理」常是規模化真正的瓶頸。

#### C3 — Embrace responsible AI principles and practices
- **目標**：能說明負責任 AI 為何重要，並把六大原則落地成治理。
- **六大原則**（投影片 21，每個都配一個「失敗案例」加深印象）：
  - **Fairness**（貸款模型性別歧視）、**Reliability & Safety**（自駕系統失效）、**Privacy & Security**（醫療資料外洩）、**Inclusiveness**（無語音輸出排除視障）、**Transparency**（金融建議無法解釋）、**Accountability**（人臉辨識誤判責任不清）。
  - 治理系統：Chief Ethics Officer（集中）／Ethics office／Ethics committee（分散）→ 建議**混合式**、對董事會負責、有預算與職權。
  - 落地實務：提供資源與訓練、建立**集中式 AI 清冊**、開發自動化合規工具、與內外部利害關係人協作。
  - Responsible AI at Microsoft：Senior Leadership Team、Office of Responsible AI、Responsible AI Champs、全員訓練。
- **易踩雷**：把偏誤檢查當「一次性打勾」是常見錯誤——強調**持續**過程。

#### C4 — Scale AI in your organization
- **目標**：從試點走向全組織規模化採用。
- **關鍵講點**：
  - **Becoming Frontier 四步**：Educate & inspire → Assess readiness（Secure AI Readiness Assessment）→ Map your AI journey（CoE、治理護欄、資料/平台 landing zone；可省成本達 30%）→ Start building（收斂 3–5 個高價值使用情境）。
  - **組織角色**：Line of Business leader、Chief Digital Officer、HR Leader、IT Leader 的分工。
  - **賦能業務使用者**與**主題專家**：用內建於 M365/Dynamics/Bing 的模型與 Power Platform／Foundry **無需寫程式**就能建應用。
  - 引用 Work Trend Index《Frontier Firm》：47% 領導者把「既有員工再訓練」列為未來 12–18 個月首要人力策略。
- **易踩雷**：規模化 ≠ 到處開試點；強調「用價值與上市時間排序的**聚焦組合**」。

**C 路徑 Knowledge check 解答（投影片 03/34）**
1. 最能描述 Microsoft 365 Copilot 與 AI agents 如何轉變工作？→ **加速生產力、改善流程並促成功能性轉型**。
2. 哪個原則確保 AI 以設計對相似的人與情況一視同仁？→ **Fairness（公平性）**。
3. 四步框架的主要目的？→ **超越試點，達成可規模化、可衡量的商業影響**（投影片動畫標示的正解為此選項；「提供連結商業成果的結構化路線圖」語意雖相近，但非動畫標示的答案）。

---

## 4. Demo 對應

- 主要 Demo：**Teams 會議全流程（會前／會中／會後）**，最適合放在 **B1**。
- 三個情境（NPI 新產品導入、供應鏈風險管理、QBR 季度業務回顧）可依學員產業擇一深入。
- 逐步操作、範例檔案、租戶／授權需求、重設與備援方案，全部見 **[`demo-environment.md`](demo-environment.md)**。
- 若無法現場連線 Copilot，改用 `demo-environment.md` 的備援（預錄畫面／截圖）。

---

## 5. FAQ / 常見學員提問

- **「Copilot 會不會拿我們的資料去訓練模型？」**→ 不會；用 Enterprise data protection 說明商業資料保護與權限邊界。
- **「Copilot 和 ChatGPT 差在哪？」**→ Copilot 結合**組織資料 + Microsoft Graph + 企業級安全合規**。
- **「要先買 E5 嗎？」**→ 視情境；帶到授權比較與「先試點再擴大」。
- **「我們沒有資料科學團隊也能導入嗎？」**→ 可；區分「買 Copilot（生產力）」與「建 Azure AI（客製）」兩條路。
- **「AI 幻覺怎麼辦？」**→ Grounding／RAG、人為審核、治理與稽核。

---

## 6. 講師須知與時效性

- **投影片版本＝2025 年 12 月**；投影片結構對應 Learn 的 3 路徑 / 8 模組，但**部分細節（產品名稱、授權方案、模型、Azure AI Search 等命名）可能已隨 Learn 於 2026 年更新而略有差異**。授課時**以 Learn 現行內容為準**並說明差異。
- ⚠️ **考試 AB-731（英文版）預計於 2026-07-22 更新**；每次開課前請重新檢視 [study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ab-731)。
- 投影片講者稿內有兩處小瑕疵（不影響授課）：Deck 02 第 2 頁備忘稿誤貼了 `leverage-ai-tools` 連結；Deck 03 第 27 頁備忘稿有一個網址錯字 `…/raining/modules/scale-ai/`。正確模組連結見 `../README.md`。
- **Achievement Code vs 認證**：完成課程 → 拿 **Achievement Code**（完課徽章）；**認證** *AI Transformation Leader* 需另外**通過考試 AB-731**（Pearson VUE，45 分鐘，700/1000）。務必向學員清楚區分兩者。

---

## 7. 開課前檢查清單（Preflight）

- [ ] 更新 `../README.md` 的 **Date** 與 **Course ID（ESI 交付編號）**、確認 `aka.ms/ab731survey` 可開啟。
- [ ] 確認 Demo 租戶已具備 **Microsoft 365 Copilot** 授權，且 `demo-environment.md` 的範例檔案已上傳到正確位置。
- [ ] 重新檢視考試 study guide（尤其在 2026-07-22 之後）。
- [ ] 投影片自訂頁（講師介紹、課程行程）已填入並刪除「Trainers:」提示備忘稿。
- [ ] 準備 Demo 備援（預錄／截圖），以防現場連線失敗。
- [ ] 檢查客戶專屬 Demo 資料的授權與敏感性（見 `demo-environment.md`）。
