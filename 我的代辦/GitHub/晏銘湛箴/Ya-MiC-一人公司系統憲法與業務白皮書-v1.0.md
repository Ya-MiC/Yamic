# Ya-MiC 一人公司系統憲法與業務白皮書
## Ya-MiC One-Person Company Constitution & System Whitepaper

> **版本 / Version**：v1.0-candidate
>
> **狀態 / Status**：CANDIDATE-WHITEPAPER — 等待創辦人逐章人類校對，不代表公司已成立、產品已完成、客戶已存在或任何功能已上線。
>
> **創辦人 / Founder**：曹晏銘 / YanMing Cao / Ya-MiC / 晏銘 / 湛箴
>
> **主要語言 / Primary languages**：繁體中文、English（目前以繁中為正式工作語言；對外 README 可另設完整英文版）
>
> **最後更新 / Last updated**：2026-09-03
>
> **文件目的 / Purpose**：這不是一份空泛的品牌文案，也不是一個把所有想法硬說成已完成的融資簡報。它是一份真實的、模組化的、一人公司「憲法＋業務白皮書」：清楚區分已存在、正在治理、未來可做、需要人類校對、不可由 AI 逕自決定的事情。

---

# 讀者導覽

本文件同時服務四類人，但同一段內容不能混淆四種身份：

| 讀者 | 最應先讀 | 他需要知道什麼 |
|---|---|---|
| 創辦人 Ya-MiC | 第 1、3、5、16、18 章 | 哪些是事實、現在做什麼、什麼不可越權 |
| 未來開源使用者 | 第 2、4、6、7、14、19 章 | 這個系統能做什麼、不能做什麼、怎麼參與 |
| 未來協作者/開發者 | 第 8–15、17、20 章 | 模組如何拆分、資料如何流動、貢獻從哪開始 |
| 未來審計行業使用者 | 第 21–26 章 | 湛箴的問題定義、四頁工作流、資料安全邊界 |

---

# 目錄

- 1. 創辦人聲明：這個系統為什麼存在
- 2. 一句話定位、願景、使命與非目標
- 3. 真實現況：已存在、正在做、尚未開始
- 4. 兩個產品、一套共同底座
- 5. 一人公司憲法：人類主權與決策規則
- 6. 產品 A：Ya-MiC OS 的使用者價值
- 7. 產品 A 的完整模組地圖
- 8. 模組 00：系統憲法與決策台帳
- 9. 模組 10：多來源資產接入層
- 10. 模組 20：分類、標籤與收藏系統
- 11. 模組 30：資產卡、關係圖、知識圖譜與星雲圖
- 12. 模組 40：GitHub Actions 與自動化治理
- 13. 模組 50：儀表盤、資訊架構與美學工程
- 14. 模組 60：桌面版、離線優先與本機檔案工作區
- 15. 模組 70：登入、OAuth、權限與資料接入同意
- 16. 模組 80：資料分級、隱私、安全與回滾
- 17. 模組 90：Skill 封裝、Agent 協作與可攜式工作流
- 18. 文件治理：如何防止 Markdown、規則與 AI 草稿打架
- 19. 開源模式、使用者分層與未來收入邏輯
- 20. 工程流程：從想法到可用功能的唯一通道
- 21. 產品 B：湛箴的行業問題與真實邊界
- 22. 湛箴四頁工作台
- 23. 文件、表格、OCR、知識庫與資料流
- 24. 審計資料、證據、人工校對與 AI 邊界
- 25. 技術棧、免費資源與成本階梯
- 26. 路線圖：現在、下一階段、未來模組
- 27. 人類校對清單與待定決策
- 附錄 A：三個核心倉庫與文件地圖
- 附錄 B：分類字典
- 附錄 C：AI 行動紀錄格式
- 附錄 D：術語白話表

---

# 1. 創辦人聲明：這個系統為什麼存在

Ya-MiC 不把 GitHub 看成「只給程式設計師放程式碼的網站」，也不把 Notion 看成「只用來記筆記的軟體」。對一個仍在學習、同時接觸商務數據分析、會計、審計、跨境電商、影片內容、AI Agent、雲端部署與個人知識管理的人來說，真正的困難不是沒有工具，而是工具、文件、想法與歷史分散在不同地方，最後沒有人知道：

```text
我有什麼？
它是什麼？
它和什麼有關？
它現在要不要做？
它未來會不會有用？
誰可以改它？
AI 做過什麼？
我為什麼當時做了這個決定？
```

Ya-MiC OS 從這個問題出發：先讓創辦人自己看懂全部數位資產，再讓未來使用者也能看懂自己的 GitHub、Notion、Google 工作資料與本機文件。

湛箴從另一個更具體的問題出發：會計、審計、企業內控與報告工作，往往不是缺一個「會聊天的大模型」，而是缺一個能保留原始資料、區分內容和格式、讓人類真正校對、把版本與責任留痕的工作台。

這兩件事有共同的底層價值：

```text
人類原始語言不能丟。
原始資料不能被 AI 覆寫。
AI 可以加速理解與草擬，但不能冒充最終責任人。
所有重要決策都要能被回看。
系統必須從「我一個人也能用」開始，而不是假裝自己已經是大公司。
```

---

# 2. 一句話定位、願景、使命與非目標

## 2.1 一句話定位

> **Ya-MiC 是一套讓個人、知識工作者與未來行業使用者，把分散的數位資產、工作記錄、文件與 AI 協作流程，轉化成可理解、可追溯、可視覺化、由人類掌控的工作系統。**

## 2.2 願景

讓任何一個不是全職工程師的人，也能：

- 看清自己的 GitHub、Notion、Google 文件與本機資料究竟有哪些資產。
- 不因為工具太多、檔案太亂、AI 回覆太多而失去對工作的控制。
- 用卡片、圖譜、流程圖與資料流，而不是一堆孤立目錄，理解自己的工作。
- 讓 AI 幫忙規劃、分類、草擬與找關係，但保留最後的人類校對與決策。

## 2.3 使命

```text
第一使命：先讓 Ya-MiC 自己不再被分散的資料與工具困住。
第二使命：把這套能力做成別人也能下載、理解、使用與改進的開源工具。
第三使命：在審計/會計領域，探索一套以證據、人類校對與專業流程為核心的智能工作台。
```

## 2.4 非目標

Ya-MiC 現階段不承諾、也不假裝具備以下能力：

- 不是企業 ERP。
- 不是正式審計軟體，不輸出具有法律/審計簽字效力的結論。
- 不是自動交易、投資建議或收益承諾工具。
- 不是要取代 GitHub、Notion、Google Drive、WPS 或任何既有平台。
- 不是「所有資料都自動上雲」的監控產品。
- 不是目前就要發幣、ICO、處理支付或進行金融產品營運的公司。
- 不是用漂亮儀表盤掩蓋資料不準確的展示工具。

---

# 3. 真實現況：已存在、正在做、尚未開始

所有外部讀者都必須先看這一章。產品描述若不區分真實狀態，就會變成誤導。

| 層級 | 內容 | 真實狀態 |
|---|---|---|
| 已存在 | `Ya-MiC/ya-mic-os` GitHub 倉庫、HTML 儀表盤、Netlify 網站、GitHub Topics 第一輪治理 | 已存在，需持續整理/修正 |
| 已存在 | GitHub 自有倉庫的第一輪 `domain-*`、`role-*`、`stage-*`、`env-*`、`risk-*` Topics | 已執行，仍需人工持續校正 |
| 已存在 | GitHub Star Lists 與星標分類建議表 | List 存在；一部分需人類在網頁手動分類 |
| 已存在 | `Ya-MiC/ya-mic-growth-log`，保存早期 Skill、原始想法、流程圖與成長記錄 | 已存在，定位需逐步整理 |
| 已存在 | `Ya-MiC/zhanzhen--audit-agent-blueprint`：審計智能體研究、四頁流程、技術調研文件 | 已存在，但屬於構想/研究，不是產品 |
| 正在做 | GitHub 倉庫分類、Stage 標籤、錯誤 env 標籤修正、Star List 整理 | 進行中 |
| 下一步 | `repo-index.json`、資料模型、星雲圖、文件級分類 | 尚未開始工程實作 |
| 未來 | Tauri 桌面版、Google/Notion OAuth、跨平台資料接入 | 尚未開始 |
| 未來 | 湛箴四頁工作台、OCR、RAG、企業本機部署、行業模板 | 尚未開始 |
| 未定 | 公司註冊、收費、專利、支付、微信登入、簡訊、發幣/代幣 | 不是現階段決策 |

## 3.1 誠實描述規則

```text
已存在        → 可以寫「已建立」「已部署」「目前可見」。
正在做        → 可以寫「正在整理」「正在驗證」。
設計完成      → 只能寫「已完成架構設計」，不可寫「已完成產品」。
未開始        → 寫「未來模組」「研究方向」「候選方案」。
未定          → 寫「需創辦人決策」，不可自行替創辦人決定。
```

---

# 4. 兩個產品、一套共同底座

```text
                     Ya-MiC 共用底座
  人類主權 / 分類字典 / 資產卡 / 圖譜 / 版本卡 / 文件治理
                                  │
               ┌──────────────────┴──────────────────┐
               │                                     │
        產品 A：Ya-MiC OS                     產品 B：湛箴
        個人數位資產與第二大腦                審計/會計智能工作台
        現在正在做                             未來研究與構想
```

## 4.1 產品 A：Ya-MiC OS

Ya-MiC OS 是現有產品。它先服務創辦人本人，未來才可能服務其他 GitHub 使用者。它的核心是：

```text
看見 → 分類 → 連結 → 理解 → 校對 → 持續更新
```

它不只是 GitHub Dashboard；GitHub 是第一個入口。未來可以接 Notion、Google Sheets、Google Drive、飛書、WPS/金山、Excel、本機檔案與其他來源。

## 4.2 產品 B：湛箴

湛箴是未來產品研究。它的核心不是「讓 AI 自動做審計」，而是：

```text
把原始材料、內容草稿、格式處理、人類審核、版本留痕與最終會簽拆開，
讓專業人員更容易看清資料、減少機械重複工作，但不失去專業責任。
```

## 4.3 共用但不混用

| 共用的能力 | 不可混用的東西 |
|---|---|
| 卡片化版本記錄 | Ya-MiC 個人資料不得混入企業審計資料 |
| 知識圖譜和流程圖 | GitHub 公開資料不得被當成企業證據 |
| Human Review 人類確認 | 湛箴客戶資料不得拿去訓練或展示 Ya-MiC OS |
| 文件分類、標籤字典 | 產品 A 的個人 OAuth 不代表產品 B 自動可讀企業資料 |
| AI 先規劃、人類校對 | 產品 B 不能因為 AI 生成就聲稱審計結論有效 |

---

# 5. 一人公司憲法：人類主權與決策規則

## 5.1 一人公司不是「一個人要同時做完所有事」

Ya-MiC 是一人公司方向，不等於創辦人必須理解、執行並承擔每一個技術、法律、財務與設計決定。系統必須承認分工：

```text
創辦人：定義問題、價值取向、是否公開、是否繼續、最終確認。
AI：整理資訊、提出候選方案、草擬文件、分析關係、生成可檢查的工程提案。
工具/自動化：執行重複、低風險、可驗證的工作。
未來專業人士：法律、會計、審計簽字、資安、商標/專利、客戶資料合規。
```

## 5.2 不可違反原則

1. **先理解，再整理；先保留，再決策。**
2. AI 的建議不是創辦人的決定。
3. 原始人類語言不覆寫，只能增加解釋、連結與版本。
4. 任何刪除、公開、轉移、覆寫、付款、Token、Secret、部署、權限變更都需要人類明確確認。
5. 若沒有足夠證據，系統提高不確定性，不補故事。
6. 同一問題只能有一份正式規範；其他版本都要知道自己是草稿或歷史。
7. 任何外部使用者都必須能知道哪些資料在本機、哪些資料在雲端、哪些資料 AI 能看、哪些資料 AI 不能看。

## 5.3 AI 全規劃、人類校對模式

這是 Ya-MiC 的核心互動方式：

```text
AI 可先產生完整分類、完整流程、完整草稿、完整候選面板。
↓
介面必須清楚標示：AI 草稿 / 未確認。
↓
人類以 ✓ 確認、✗ 修改、? 存疑、A-E 裁決等方式標記。
↓
AI 只修正被指出的部分，保留已確認內容與原始痕跡。
↓
人類確認後，才進入正式狀態或執行寫入。
```

---

# 6. 產品 A：Ya-MiC OS 的使用者價值

## 6.1 第一個使用者：創辦人自己

創辦人目前有 63 個自有 GitHub repositories、50 個星標，且 Notion、GitHub、文件與外部參考分散。第一個價值不是「讓別人看了覺得酷」，而是：

- 一眼知道目前有哪些倉庫、哪些是核心、哪些是記錄、哪些是純參考。
- 新增倉庫後，不會三個月不管，最後忘記用途。
- Star 不再只是「按了星但再也找不到」；可以按研究、候選採用、美學、Agent、基礎設施等角度回找。
- GitHub 與 Notion 不是兩套記憶，而能互相連結。
- 未來 `.md`、`.yml`、`.png`、`.xlsx`、`.csv`、`.pdf`、`.docx`、`.pptx` 文件也可被同一個系統索引。

## 6.2 未來使用者：非工程師 GitHub 使用者

未來的目標不是讓每個人都學會 Git 命令，而是提供：

```text
輸入 GitHub 使用者名稱
→ 看公開倉庫
→ AI 提供分類草案
→ 使用者確認/修正
→ 看自己的圖譜、Star、Issue、PR、文件與關係
```

進階使用者才需要 OAuth；只看公開 GitHub Profile 的使用者，不需要登入。

## 6.3 未來使用者：個人知識工作者

有人工作內容主要在 GitHub；有人在 Notion、Google Drive、飛書、WPS、Excel 或紙本。Ya-MiC OS 的長期價值是：不同來源進來後，都變成**可追溯資產卡**，而不是強迫所有人遷移到一個新平台。

---

# 7. 產品 A 的完整模組地圖

```text
Ya-MiC OS
│
├── 模組 00　系統憲法與決策台帳
├── 模組 10　資料接入（GitHub / Notion / Google / 本機）
├── 模組 20　分類與收藏（Topics / Star Lists / filetype）
├── 模組 30　資產卡與圖譜（關係、星雲、標籤索引）
├── 模組 40　自動化治理（GitHub Actions、提醒、同步）
├── 模組 50　儀表盤與美學（Web/PWA）
├── 模組 60　桌面版與本機檔案工作區（Tauri）
├── 模組 70　登入/OAuth/同意管理
├── 模組 80　資料安全、權限、備份與回滾
└── 模組 90　Skill 封裝與 Agent 工作流
```

每個模組都必須有：

```text
目的 / 使用者 / 輸入 / 輸出 / 資料位置 / 免費方案 / 付費觸發條件 /
AI 能做什麼 / 人類必須校對什麼 / 現在狀態 / 不做什麼
```

---

# 8. 模組 00：系統憲法與決策台帳

## 8.1 目的

防止「新增一份文件，卻不知道它和前面十份文件是什麼關係」。

## 8.2 內容

```text
系統角色地圖
已確認決策（Decision Ledger）
未確認候選方案
模組登記冊（不是 Parking Lot）
文件版本與取代關係
每週唯一正在做的工作
```

## 8.3 模組登記冊

所有未來需求必須被保留，但每一項都要有強注釋與人類校對點：

| 模組 | 為什麼未來需要 | 現在為什麼不做 | 啟動條件 | 人類校對點 |
|---|---|---|---|---|
| Google OAuth | 匯入舊 Docs/Sheets/Drive 工作記錄 | 尚未有桌面/資料模型基礎 | repo-index/content-index 定稿 | OAuth scopes、資料授權畫面 |
| Notion OAuth | 同步 Notion 第二大腦 | 現有 Notion 連結先可用 | GitHub 模組穩定後 | 哪些 workspace/page 可讀 |
| Tauri 桌面版 | 像 v2rayN 一樣下載即用、本機檔案處理 | Web 資料模型未定 | Web 面板資料結構穩定 | Windows/Linux/macOS 範圍 |
| OCR | 憑證、發票、紙本資料數位化 | 湛箴尚未進工程 | 父親確認第一個真實工作流 | 原件保存、脫敏、本機/雲端 |
| 湛箴登入 | 未來客戶與資料授權 | 尚未有客戶與產品 | 湛箴 Prototype 前 | Google/Apple/微信/手機範圍 |
| 專利 | 保護可能的技術/流程創新 | 目前尚無可驗證實作 | 有 MVP / 專業諮詢 | 是否申請、公開前檢索 |

## 8.4 免費性

純 Markdown + GitHub 就可做，**免費**。

---

# 9. 模組 10：多來源資產接入層

## 9.1 核心原則

```text
不搬家優先：資料留在原平台，Ya-MiC OS 建索引與連結。
最低權限：只請求完成任務所需的 OAuth 範圍。
延遲接入：還沒有真正用途的來源，不先接 Token。
來源保留：任何 AI 摘要都要回鏈到原始來源。
```

## 9.2 資料來源路線

| 優先級 | 來源 | 現在狀態 | 接入方式 | 是否免費起步 |
|---|---|---|---|---|
| P0 | GitHub | 已接入/已治理 | API、GitHub CLI、GitHub Actions | 是 |
| P0 | Notion | 已接入/有主控頁 | Notion API/OAuth（未來）或現有連結 | 是 |
| P1 | Google Sheets | 未接入 | Google OAuth + Sheets API | 是，配額內免費 |
| P1 | Google Docs/Drive | 未接入 | Google OAuth + Drive API | 是，配額內免費 |
| P2 | 本機檔案 | 未接入 | Tauri 本機檔案選擇器 | 是 |
| P2 | Excel/CSV | 未接入 | 本機解析/匯入 | 是 |
| P3 | 飛書/金山/WPS/釘釘 | 未接入 | 各平台開放 API/匯出檔案 | 視平台而定 |
| P3 | 手機照片/PDF | 未接入 | 桌面同步/手機上傳/OCR | 本機方案可免費 |

## 9.3 統一資產格式

不管來源是哪裡，每個被接入的資產都要變成一張卡，不是把原始檔搬進來：

```json
{
  "asset_id": "github:Ya-MiC:ya-mic-os",
  "source": "github",
  "source_url": "https://github.com/Ya-MiC/ya-mic-os",
  "type": "repository",
  "title": "ya-mic-os",
  "created_at": "2026-08-26",
  "last_seen_at": "2026-09-03",
  "visibility": "private",
  "classification_status": "human-confirmed | ai-proposed | human-review",
  "relationships": [],
  "evidence": []
}
```

## 9.4 人類校對點

- 是否允許讀取來源。
- 是否只讀或讀寫。
- 哪些資料夾、資料庫、頁面、Google Drive Scope 可以接入。
- 是否允許 AI 摘要內容，還是只允許顯示檔名/metadata。

---

# 10. 模組 20：分類、標籤與收藏系統

分類必須分三套，不能混用。

## 10.1 GitHub Topics：分類自己的倉庫

```text
domain-*：主要做什麼
role-*：在資產組合中扮演什麼角色
stage-*：目前該怎麼對待
env-*：真正依賴的環境
risk-*：需要注意的風險
```

目前已完成第一輪 Topics 治理，但這不是最終定論。每月或每次重大變更後，可重新校對；不因為「貼了標籤」就把 AI 推論變成事實。

## 10.2 GitHub Star Lists：分類別人的倉庫

建議字典：

```text
S·研究學習              學架構/方法/知識
A·候選採用              明確考慮整合或 Fork
M·持續觀察              想追蹤更新
R·風險留意              授權/安全/維護需額外判斷
D·美學前端參考          儀表盤、視覺、圖譜、互動
G·Agent與Skill參考      Agent、Prompt、Skill、工作流
I·基礎設施工具          Docker、網路、DNS、CLI、部署
W·溝通與生活工具        溝通、個人成長、事實查核
X·待分類                新 Star 的安全入口
```

Star List 是 GitHub 平台功能；目前沒有可靠公開 API 能讓程式自動寫入。因此：AI 負責建議，人類在 GitHub 網頁點選，是正常且安全的設計，不是失敗。

## 10.3 文件類型標籤：分類任何檔案

這不應放到 GitHub Topics。它屬於 Ya-MiC OS 自己的資料層：

```text
filetype-yaml          .yml / .yaml
filetype-markdown      .md
filetype-image         .png / .jpg / .jpeg / .webp / .svg
filetype-spreadsheet   .xlsx / .xls / .csv / Google Sheets
filetype-document      .docx / .doc / Google Docs
filetype-presentation  .pptx / .ppt / Google Slides
filetype-pdf           .pdf
filetype-code          .py / .js / .ts / .rs / .java / .ps1 / .sh
filetype-config        .json / .toml / .ini / .env.example
filetype-archive       .zip / .7z / .tar.gz
filetype-audio         .mp3 / .wav / .m4a
filetype-video         .mp4 / .mov
filetype-unknown       無法識別或新格式
```

## 10.4 分類規則

```text
一個檔案/倉庫可以有多個 type/env/risk 標籤。
一個倉庫只能有一個 primary domain 與一個主要 role。
不確定 → 標記 human-review 或 unknown，不強行分類。
既有標籤優先保留；AI 建議標籤不能覆蓋人類/原專案既有規則。
```

---

# 11. 模組 30：資產卡、關係圖、知識圖譜與星雲圖

## 11.1 不是「畫好看的線」，而是四種不同圖

| 圖類型 | 回答什麼 | 範例 |
|---|---|---|
| 資產關係圖 | 這個倉庫和哪個倉庫有關？ | `zhanzhen-web` → 前端；`zhanzhen-server` → 後端 |
| 工作流圖 | 一件事先做什麼、後做什麼？ | 新倉庫偵測 → AI 分類草案 → 人類確認 |
| 資料流圖 | 資料從哪裡進、變成什麼、到哪裡去？ | GitHub API → `repo-index.json` → Web Dashboard |
| 知識圖譜 | 想法、研究、文件、產品、任務如何互相引用？ | 原始創意 → 湛箴藍圖 → OCR 模組研究 |

## 11.2 資產卡必填欄位

```yaml
asset:
  title:
  source:
  source_url:
  type:
  owner:
  visibility:
  one_sentence_value:
  primary_domain:
  role:
  stage:
  file_types: []
  environment: []
  risk: []
  related_to: []
  depends_on: []
  evidence: []
  status: ai-proposed | human-confirmed | human-review
  last_reviewed_at:
```

## 11.3 關係類型字典

```text
depends-on        技術/資料依賴
used-by           被誰使用
frontend-for      某系統前端
backend-for       某系統後端
planned-for       為未來產品準備
inspired-by       靈感/方法來源
forked-from       Fork 上游
related-to        有關但無強依賴
documented-by     被哪份文件描述
replaced-by       被哪個資產取代
```

## 11.4 目前已知關係（只寫可驗證的）

```text
zhanzhen-web       frontend-for  zhanzhen
zhanzhen-server    backend-for   zhanzhen
zhanzhen-handover  documented-by / related-to zhanzhen
zhanzhen--audit-agent-blueprint planned-for zhanzhen
ya-mic-os          related-to    ya-mic-growth-log
ya-mic-growth-log  documents     人類原始想法與 Skill 演化
```

其他關係在沒有實際 README、程式或創辦人確認前，不得假裝已知。

---

# 12. 模組 40：GitHub Actions 與自動化治理

## 12.1 自動化不是「讓 AI 自己亂改」

自動化只適合做三種事：

```text
偵測（發現新資料）
整理草稿（產出待確認資料）
提醒（通知人類做決定）
```

自動化不適合直接做：

```text
刪除、公開、改名、移除標籤、覆寫 README、修改權限、發布產品、花錢。
```

## 12.2 建議的 Actions 分層

| Workflow | 觸發 | 做什麼 | 是否可自動寫入 |
|---|---|---|---|
| `detect-new-repos.yml` | 每日/手動 | 發現無 `domain-*` 的新 repo，開提醒 Issue | 只可新增 Issue |
| `sync-repo-metadata.yml` | 每 6 小時/每日 | 讀 GitHub metadata，更新候選快照 | 可只更新 `data/` 的機器資料 |
| `validate-taxonomy.yml` | PR/手動 | 檢查一個倉庫是否缺 domain/role/stage | 不寫入，只報告 |
| `render-dashboard-data.yml` | metadata 更新後 | 將 JSON 轉成 Dashboard 可讀資料 | 可更新生成檔，但不改人類內容 |
| `report-weekly-governance.yml` | 每週 | 彙整新增 repo、未分類項、風險提醒 | 只可開/更新一張週報 Issue |
```

## 12.3 Issue、Project、Milestone、Label 的正確分工

| GitHub 功能 | 唯一用途 | Ya-MiC OS 怎麼用 |
|---|---|---|
| Topics | 分類整個 repository | `domain-*` 等五維標籤 |
| Star List | 分類別人的 Star | S/A/M/R/D/G/I/W/X |
| Issue | 一張具體問題、任務或人類裁決卡 | Human Review、Bug、功能需求 |
| Label | 幫 Issue 分類 | `governance`、`human-review`、`type:bug`、`priority:high` |
| Project | 多張 Issue 的工作看板 | 只用於「本週要做什麼」，不是資產圖譜 |
| Milestone | 一組 Issue 對應一個版本/日期目標 | 產品真有 v0.1/v0.2 時才用 |
| Ya-MiC OS Dashboard | 自己的資產全景、圖譜、跨平台資料 | 這才是你要的真正面板 |

---

# 13. 模組 50：儀表盤、資訊架構與美學工程

## 13.1 導覽架構

```text
主導航（第一層）：
GitHub | Notion | Google | Files | Graph | Review | Settings

GitHub（第二層）：
Repositories | Starred | Forks | Issues | Pull Requests | Collections | Taxonomy

Files（第二層，未來）：
All Files | Markdown | YAML | Images | Spreadsheets | Documents | PDF | Code | Unknown

Graph（第二層）：
Repository Map | Knowledge Graph | Workflow Map | Data Flow | Tag Index
```

## 13.2 美學原則

```text
專業：資料、風險、來源、狀態清楚可見。
俏皮：只用在完成回饋、進度、輕量互動，不干擾專業資料。
透明：不藏風險、不藏 AI 草稿、不藏資料來源。
克制：不使用幣安/CZ 式金黑投機感、倒數壓迫感或收益暗示。
溫暖但中立：不用 PayPal 式冷漠制式，但也不假裝情緒陪伴。
```

## 13.3 設計代幣（正式候選）

```css
--ymc-ink-900: #14171A;     /* 深色資料背景 */
--ymc-ink-800: #1E2226;
--ymc-lime-500: #7ED957;    /* 行動、完成、成長 */
--ymc-lime-600: #63B843;
--ymc-amber-500: #F2A93B;   /* 待裁決 */
--ymc-brick-500: #E2593C;   /* 風險 */
--ymc-paper-000: #FDFBF6;   /* 暖白 */
--ymc-gray-400: #A8A296;
```

這不是照搬 Wise、Duolingo、Nexo 的品牌色；它只借鑑「清楚色彩語義、資料卡片、適度正向反饋」的設計邏輯。

## 13.4 Dashboard 必須先做到的四件事

```text
1. 所有倉庫可以篩選：domain / role / stage / env / risk。
2. 所有 Star 可以按 List 或建議 List 看。
3. 點倉庫可看資產卡：用途、關係、來源、目前階段。
4. Graph 頁可看關係，但任何線都標示「已驗證 / AI 推測 / 待確認」。
```

---

# 14. 模組 60：桌面版、離線優先與本機檔案工作區

## 14.1 為什麼需要桌面版

你想要的是 v2rayN 類型的使用感：下載、雙擊、能看本機文件、少設定、可離線，不是只打一個網址。

## 14.2 選型

```text
候選：Tauri
理由：可將現有 HTML/CSS/JS 包成 Windows/macOS/Linux 桌面 App；
      可使用系統檔案選擇器；可讀取使用者明確授權的本機資料夾；
      體積通常比 Electron 小；開源。
```

## 14.3 本機檔案模組的安全邊界

```text
預設：程式看不到任何文件。
使用者手動選擇資料夾：程式只索引該資料夾。
AI 預設只看檔名、類型、大小、時間；
需要讀內容時，逐次提示使用者同意。
原始檔不移動、不刪除、不覆寫。
所有產出放到獨立 output/ 或 processed/ 目錄。
```

## 14.4 免費性

Tauri、Rust、Node.js、HTML/CSS/JS 都可免費使用。真正的成本是工程時間，而不是軟體授權費。

---

# 15. 模組 70：登入、OAuth、權限與資料接入同意

## 15.1 現階段原則

```text
產品 A 現在不需要登入。
看 Ya-MiC 自己的公開/本地 Dashboard，不需要 OAuth。
只有當「別人要生成他自己的私人面板」或「要接入 Google/Notion 私有資料」時，才需要登入。
```

## 15.2 第一批登入來源（未來順序）

```text
1. GitHub OAuth：讓使用者讀自己的 repo、Star、Issue、PR。
2. Google OAuth：讓使用者選擇是否讀 Drive/Docs/Sheets。
3. Notion OAuth：讓使用者選擇哪個 workspace/page/database 可接入。
```

## 15.3 同意畫面必須說人話

不能只說「Allow access」。要說：

```text
你正在允許 Ya-MiC OS：
- 讀取哪些來源？
- 讀取哪些資料類型？
- 是只讀，還是可以寫回？
- 資料留在本機、雲端還是原平台？
- AI 能否讀取內容？
- 如何隨時撤銷授權？
```

## 15.4 產品 B 的登入不是現在的工程項

Google、Apple、郵箱驗證碼、手機號、微信、支付寶、簡訊與電信商，屬於湛箴真正進入 Prototype/Pilot 後才啟動的模組。它們被保留在模組登記冊，不代表現在要申請 Token、花錢或建立公司。

---

# 16. 模組 80：資料分級、隱私、安全與回滾

## 16.1 三級資料分級

| 等級 | 資料例子 | 是否可上雲 | AI 可否讀取 |
|---|---|---|---|
| L1 公開 | 公開 GitHub repo、公開 README、公開政府文件、公開論文連結 | 可以 | 可以，但必須保留來源 |
| L2 個人私有 | 私有 repo metadata、私人 Notion、個人 Sheets、學習記錄 | 預設不上傳；人類選擇後才可 | 預設只看 metadata，讀內容需確認 |
| L3 企業/客戶 | 憑證、賬套、審計底稿、客戶報告、身份資料 | MVP 階段不得上雲 | 預設不可；未來需企業確認、本機部署/合規方案 |

## 16.2 原始資料保留

```text
原檔：永遠不覆寫。
AI 草稿：另存，不覆寫原檔。
人工確認版：另存為 approved/ 或 signed-off/。
輸出檔：另存為 output/，包含來源/時間/版本。
```

## 16.3 回滾

每個可寫入模組都要有回滾方式：

```text
GitHub 檔案 → Git history / Pull Request
Notion 頁面 → 版本歷史/人工確認
本機文件 → 原檔不動 + 產出另存
分類標籤 → 改回人類確認的上一版本
```

---

# 17. 模組 90：Skill 封裝、Agent 協作與可攜式工作流

## 17.1 三個既有 Skill 的定位

| Skill | 真正用途 | 不應做什麼 |
|---|---|---|
| GitHub Portfolio OS | 倉庫/Star/Fork/Topics/評分/治理 | 不應充當全部第二大腦或企業系統 |
| 美學工程 × 登入系統 | UI、PWA、登入、資料同意、安全提示 | 不應自行決定產品優先級或公司戰略 |
| 人類主權第二大腦 OS | 原始語言、兩產品邊界、決策、資料主權 | 不應變成重複的工程文件集合 |

## 17.2 真正可安裝 Skill 的封裝規格

不是任何 `.md` 都叫 Skill。正式可安裝 Skill 要有：

```text
skills/
  github-portfolio-os/
    SKILL.md                 有 YAML frontmatter 的主入口
    README.md                繁中/英文使用說明
    references/              可選：術語/分類字典
    examples/                輸入輸出範例
    tests/                   可選：驗證範例
```

`ya-mic-growth-log` 保存思考與歷史草稿；`ya-mic-os` 未來可保存正式、可安裝的 Skill 包。兩者不可混淆。

## 17.3 Agent 的角色

```text
Repository Scout：讀 metadata，提出分類草案。
Taxonomy Reviewer：檢查標籤是否被套模板、是否有衝突。
Graph Curator：維護可驗證關係。
Documentation Editor：寫 README/白皮書草稿，不擅自定稿。
Automation Runner：執行 GitHub Actions/重複流程。
Human Decision Editor：把問題壓縮成 30 秒可回答選項。
```

任何 Agent 都不能繞過第 5 章的人類主權規則。

---

# 18. 文件治理：如何防止 Markdown、規則與 AI 草稿打架

## 18.1 所有文件頂部必填 Metadata

```markdown
> STATUS: RAW-HUMAN-LANGUAGE | DRAFT | CANDIDATE-SPECIFICATION |
>         ACTIVE-SPECIFICATION | HISTORICAL | DEFERRED-MODULE
> OWNER: Ya-MiC | AI-assisted | external-reference
> SCOPE: <本文件管什麼>
> REPLACES: none | <舊文件路徑>
> CONFLICTS-CHECKED: yes | no
> HUMAN-APPROVAL: pending | YYYY-MM-DD
```

## 18.2 文件只能有六種狀態

| 狀態 | 能否改 | 是否正式 | 用途 |
|---|---|---|---|
| `RAW-HUMAN-LANGUAGE` | 不覆寫，只增附註 | 原始材料 | 保留創辦人原話 |
| `DRAFT` | 可以改 | 否 | 思考中草稿 |
| `CANDIDATE-SPECIFICATION` | 等人類校對 | 否 | 即將成為規範的候選 |
| `ACTIVE-SPECIFICATION` | 需明確變更紀錄 | 是 | 同一議題唯一有效規則 |
| `HISTORICAL` | 不改正文 | 否 | 被新版取代但仍保留 |
| `DEFERRED-MODULE` | 可補註解 | 否 | 未來模組，不是被遺棄 |

## 18.3 「未來模組」強注釋格式

每個未來模組不能只寫「以後再做」，要寫：

```yaml
module: Google OAuth
status: deferred-module
why_it_matters: 匯入既有 Google Docs/Sheets/Drive 工作記錄
why_not_now: Ya-MiC OS 的資料模型/本機優先策略尚未定稿
prerequisite:
  - repo-index.json 正式定稿
  - 人類確認最小 OAuth scope
  - 同意畫面設計完成
human_review_required:
  - 允許讀 Drive 還是只讀 Sheets
  - 是否允許 AI 讀內容
activation_trigger: 產品 A 的 Web 資料層穩定後
```

這就是「保留未來，而不是丟進暫時不做」的具體制度。

---

# 19. 開源模式、使用者分層與未來收入邏輯

## 19.1 現在的真實狀態

Ya-MiC 尚未成立公司、尚未正式收費、尚未有客戶。任何收入模式都只是候選，不應寫成既定商業承諾。

## 19.2 開源的意義

產品 A 可以採取開源核心模式：

```text
使用者可 Fork / 下載 / 本機運行 / 自己部署。
使用者不想看廣告、不想依賴服務商，可以自行部署。
創辦人不因為開源就失去價值；價值可能來自更易用的成品、託管、模板、同步、支援、行業方案。
```

## 19.3 未來可能的分層（不是現階段收費方案）

| 層級 | 使用者得到什麼 | 成本/收入狀態 |
|---|---|---|
| Community | 原始碼、基礎本機 Dashboard、分類字典、Skill | 可開源免費 |
| Personal | 一鍵桌面安裝、個人同步、模板、較好的 UI | 未來候選 |
| Pro | 多來源接入、進階圖譜、私有資料規則、支援 | 未來候選 |
| Audit / Team | 湛箴模板、企業本機部署、審核流、權限、支援 | 未來候選，需先有真實試點 |

## 19.4 不能現在做的商業決策

```text
發幣 / ICO / 加密資產收益 / 支付 / 收費價格 / 公司註冊 / 專利申請
```

不是「禁止永遠討論」，而是現在沒有足夠產品、客戶、法務與資金條件，不能讓 AI 直接設計或執行。

---

# 20. 工程流程：從想法到可用功能的唯一通道

所有工程工作都必須走同一條路，防止「今天想到一個功能，明天多一份 md，後天多一個 repo」。

```text
人類原始想法
→ 收錄到 Growth Log（RAW-HUMAN-LANGUAGE）
→ AI 產出一頁問題定義（DRAFT）
→ 創辦人確認「是否值得進入模組登記冊」
→ 寫 Candidate Specification（只定一個模組）
→ 人類校對與批准
→ 建立 GitHub Issue（具體任務）
→ 建立分支/PR（實際工程）
→ 自動/人工驗證
→ 更新 README、Changelog、Decision Ledger
→ 標為 ACTIVE 或回到 DEFERRED-MODULE
```

## 20.1 三個硬停止點

```text
停止點 1：沒有問題定義，不寫程式。
停止點 2：沒有 Candidate Specification，不開一堆 Issue。
停止點 3：沒有創辦人批准，不覆寫、不刪除、不公開、不部署。
```

---

# 21. 產品 B：湛箴的行業問題與真實邊界

## 21.1 真實問題

會計、審計工作中的資料來源很雜：憑證照片、PDF、Excel 賬套、序時賬、企業內部報告、公開審計公告、上市公司報告、行業標準、法律合作案例。真正的痛點不是「AI 能不能生成一段話」，而是：

```text
原件在哪？
OCR 結果能不能回到原圖核對？
哪個數字來自哪個賬套？
報告草稿依據是什麼？
格式與內容是否被混在一起改壞？
誰最後確認？
匯出前是否所有責任人都看過？
```

## 21.2 湛箴的定位

> 湛箴是未來研究中的「審計/會計專家工作台」：不取代審計師的判斷，不承諾自動審計，而是讓資料、草稿、格式、人類審核、版本與會簽更清楚。

## 21.3 真實邊界

```text
目前沒有客戶。
目前沒有已部署的企業版本。
目前不能處理真實客戶資料。
目前不能聲稱可以取代鼎信諾。
「超越並取代鼎信諾」是創辦人長期目標，不是當前能力描述。
```

---

# 22. 湛箴四頁工作台

## P1：內容溝通頁

```text
目的：只處理文字、表格、數據與論證是否準確。
允許：人類與 AI 對話、標記、標注、引用來源。
禁止：把排版、字體、頁邊距等格式問題混進內容討論。
候選技術：Tiptap + Univer。
```

## P2：格式與排版頁

```text
目的：只處理格式、程式、模板、版面與輸出。
允許：AI/模板引擎處理格式。
禁止：在此頁直接改正文內容，避免內容責任與排版責任混在一起。
候選技術：docx-preview + python-docx + openpyxl + python-pptx。
```

## P3：人類純審核頁

```text
目的：讓人類在 DOCX/XLSX/PPTX/PDF 等多格式之間比對、看腦圖、節點圖、證據鏈。
當前規則：這一頁與 AI 無關。AI 不生成、不對話、不介入。
原因：建立制度性的防幻覺、防越權空間。
候選技術：react-flow / Cytoscape.js + 唯讀預覽。
```

## P4：三方會簽與匯出頁

```text
發言者：作者本人 / 好友或軟體管理員 / 具 Git 記憶和操作流程的 AI。
規則：三方完成各自確認後，才允許匯出。
版本：每次 Ctrl+S 產生卡片化版本快照，顯示時間、作者、變更摘要、來源與狀態。
```

---

# 23. 文件、表格、OCR、知識庫與資料流

## 23.1 輸入格式地圖

```text
照片：JPG / PNG / HEIC
掃描：PDF / OFD
表格：XLSX / XLS / CSV / Google Sheets / WPS 表格
文件：DOCX / DOC / Google Docs
簡報：PPTX / PPT / Google Slides
文字：Markdown / TXT
```

## 23.2 OCR 的正確位置

OCR 不是第一個產品，而是湛箴未來資料接入的一個模組：

```text
原始照片/PDF（永不覆寫）
→ 人工先脫敏（當前原則）
→ OCR 產生候選文字/表格
→ 人工回看原件校驗
→ 形成可用結構化資料
→ 才能被 AI 用於草擬或檢索
```

## 23.3 批量處理原則

創辦人提出手機拍憑證一次約 10–30 張、Excel/ERP 資料可能數千筆、辦公室 PDF 可能 100–500 頁。正確策略不是直接上 100 張照片全自動：

```text
照片：先以 10–30 張為一個批次，便於人工抽查、失敗重跑與避免手機卡住。
CSV/XLSX：可較早支援，因為它不是 OCR，主要是欄位映射與格式清洗。
大型 PDF：晚於前兩者，因為需要佇列、分頁、記憶體與結果校驗策略。
```

## 23.4 本機 OCR 候選

```text
PaddleOCR：中文 OCR 的開源候選，可本機使用。
Tesseract：通用開源 OCR 候選。
雲端 OCR API：未來可選，但真實客戶資料 MVP 階段不上雲。
```

---

# 24. 審計資料、證據、人工校對與 AI 邊界

## 24.1 知識來源的分層

| 類型 | 例子 | 可以怎麼用 | 不可以怎麼用 |
|---|---|---|---|
| 公開政府/國際資料 | 審計署、交易所公告、公開案例、標準機構 | 建檢索索引、引用來源 | 不可捏造、不把二手新聞當正式依據 |
| 公開行業資料 | 上市公司審計報告、公開披露 | 分析結構、做案例研究 | 不可冒充企業內部資料 |
| 課程/協會資料 | ACCA 課程大綱、公開準則連結 | 放連結、做學習地圖 | 不搬運受版權保護教材全文 |
| 企業資料 | 內控文件、賬套、底稿、報告 | 僅獲授權、脫敏、本機處理 | MVP 不上雲、不作訓練集、不公開 |
| AI 草稿 | 報告初稿、摘要、表格建議 | 讓人類修改與校對 | 不可當正式審計結論 |

## 24.2 AI 輸出標記

每一段關鍵輸出必須有一種狀態：

```text
FACT                 可直接追到原始來源
INFERENCE            根據事實做出的推論
HYPOTHESIS           尚待驗證的假設
AI-DRAFT             AI 草稿
HUMAN-REVIEWED       人類已檢視
HUMAN-APPROVED       指定人類已確認
```

---

# 25. 技術棧、免費資源與成本階梯

## 25.1 現在可以免費使用的部分

| 類別 | 技術/服務 | 是否免費起步 | 真實用途 |
|---|---|---|---|
| 程式碼/版本 | GitHub | 是 | repo、Issues、Actions、Release |
| 網站託管 | Netlify | 是，免費額度 | Ya-MiC OS 現有網站 |
| 靜態前端 | HTML/CSS/JS | 是 | 現有 Dashboard |
| PWA | Web Manifest + Service Worker | 是 | 安裝到桌面/手機的網頁能力 |
| 桌面打包 | Tauri | 是 | 未來 Windows/Linux/macOS App |
| 圖譜 | React Flow / Cytoscape.js | 是 | 關係圖/星雲圖/流程圖 |
| 文件編輯 | Tiptap | 是 | 湛箴 P1 候選 |
| 表格 | Univer | 是 | 湛箴 P1 候選 |
| 文件生成 | python-docx/openpyxl/python-pptx | 是 | 格式/匯出候選 |
| OCR | PaddleOCR/Tesseract | 是 | 本機 OCR 候選 |
| 自動化 | GitHub Actions | 是，個人/公開範圍內 | 偵測、同步、驗證 |
| 模型實驗 | Kaggle / Colab | 有免費額度 | 未來 QLoRA/實驗，不是現在必需 |

## 25.2 未來才可能花錢的部分

| 項目 | 何時才需要 | 為何需要 | 現在是否該買 |
|---|---|---|---|
| 自訂網域 | 需要正式對外品牌時 | 比 Netlify 預設網址專業 | 不急 |
| VPS | 需要自托管 n8n/Dify/Logto/後端時 | 產品 B 或進階同步 | 不急 |
| 大模型 API | 真正有大量 AI 功能/使用者時 | 草擬、審校、檢索 | 先按量試驗 |
| 簡訊 | 中國手機登入有真實需求時 | OTP | 不急 |
| 微信登入認證 | 有企業主體與中國客戶時 | 企業版登入 | 不急 |
| Apple 開發者帳號 | 上架 iOS App 時 | Sign in with Apple / App Store | 不急 |
| 法律/專利顧問 | 有可驗證 MVP 或商業洽談時 | IP/資料/合同 | 不急但未來重要 |

## 25.3 模型使用的慎重原則

高能力模型不是因為貴或便宜才用，而是因為「這個錯誤會不會影響整個系統」。

```text
值得深度模型審查：系統憲法、資料權限、跨模組架構、刪除/覆寫/公開前的檢查。
不值得深度模型燒 token：批量加 Topic、固定格式表格、讀取 metadata、重複性的檔案重新命名。
不應現在用模型做：未有需求證明的湛箴全部工程、代幣/ICO/支付架構。
```

---

# 26. 路線圖：現在、下一階段、未來模組

## Phase 0：治理穩定（現在）

```text
目標：不是加功能，而是確認「什麼是正式的、什麼是草稿」。

完成條件：
- 本白皮書經創辦人校對為 ACTIVE-SPECIFICATION 或有明確修訂清單。
- GitHub Topics 第一輪分類有正式字典與校對紀錄。
- Star List 手動分類完成或至少 X·待分類清楚存在。
- 三個核心倉庫的 README/Description 不再互相矛盾。
```

## Phase 1：Ya-MiC OS 資料模型（下一階段）

```text
目標：讓面板不再只是靜態卡片牆，而是真正有一個可擴展資料層。

只做：
- repository-taxonomy.json（分類真相表）
- repo-index.json（資產卡/關係）
- starred-watchlist.json（Star 建議與確認狀態）
- 首張 Repository Relationship Map

不做：
- OAuth
- Tauri
- OCR
- 湛箴程式碼
```

## Phase 2：Ya-MiC OS 介面可用化

```text
目標：把資料模型渲染成清楚可用的 Dashboard。

只做：
- Repositories / Starred / Graph / Review 四個核心頁。
- domain/role/stage/env/risk 篩選。
- AI 建議 vs 人類確認狀態。
- 可點開資產卡，看來源與關係。
```

## Phase 3：本機桌面版與檔案索引

```text
目標：Tauri 封裝，使用者下載即可打開；開始做本機檔案類型索引。

前提：Phase 1/2 的資料模型已穩定。
```

## Phase 4：OAuth 與多來源接入

```text
目標：GitHub/Google/Notion 資料接入。

前提：同意畫面、最小權限、資料分級、撤銷機制都有設計。
```

## Phase 5：湛箴研究轉 Prototype

```text
目標：不是全功能審計軟體，而是先跑通一條人工可驗證的流程。

候選最小流程：
公開/模擬 Excel 或 CSV → P1 內容校對 → P2 模板匯出 → P3 人類審核 → P4 版本卡與會簽。

OCR、真實客戶資料、手機批拍、企業登入，全部後移到有真實需求、明確授權與安全方案後。
```

---

# 27. 人類校對清單與待定決策

本文件不是要你一次決定人生，只要把「誰能決定」留清楚。

## 必須由創辦人回答

| ID | 問題 | 現在安全預設 |
|---|---|---|
| H-01 | 本文件是否可升級為 `ACTIVE-SPECIFICATION v1.0`？ | 仍是候選白皮書 |
| H-02 | `ya-mic-growth-log` 是否完全公開？ | 維持現有可見性，不自動更動 |
| H-03 | Skill 1/2/3 的最終正式版要放在哪個倉庫？ | 不搬移舊文件，只建立索引 |
| H-04 | Star List 是否採用 S/A/M/R/D/G/I/W/X 命名？ | 不刪現有 List，只可新增 |
| H-05 | Ya-MiC OS 的第一個正式介面是否只做 GitHub + Notion？ | 是；Google 放 Phase 4 |
| H-06 | `repo-index.json` 的第一版是否只收錄核心 15 個倉庫？ | 是；不要一開始塞所有 63 個深度關係 |

## 需要未來專業人士參與

```text
企業客戶資料處理、審計責任、數據跨境、公司/稅務、商標、專利、支付、
微信/簡訊合規、代幣/ICO 等，不由 AI 或本白皮書做最終判定。
```

---

# 附錄 A：三個核心倉庫與文件地圖

```text
Ya-MiC/
├── ya-mic-os/
│   ├── README.md                  產品 A 對外入口
│   ├── public/data/               面板資料快照
│   ├── docs/                      正式產品規範與使用文件
│   ├── .github/workflows/         自動化
│   └── skills/（未來）            正式可安裝 Skill 包
│
├── ya-mic-growth-log/
│   ├── 00-system-constitution.md  本白皮書確認後的正式位置
│   ├── 90-raw-human-language/     原始人類語言（不覆寫）
│   ├── 91-historical-drafts/      歷史 Skill/草稿
│   ├── 92-decision-ledger/        決策台帳
│   └── 晏銘湛箴/                  湛箴相關歷史/思考材料
│
└── zhanzhen--audit-agent-blueprint/
    ├── README.md                  湛箴構想入口
    └── docs/                      原始創意、理解、調研、未來架構
```

> 注意：這是**目標文件地圖**，不是要求現在立刻移動檔案。移動現有檔案會改變 Git 路徑，必須先列 ChangeSet、由人類確認後執行。

---

# 附錄 B：分類字典（摘要）

```text
GitHub repositories：
domain-* / role-* / stage-* / env-* / risk-*

Star Lists：
S·研究學習 / A·候選採用 / M·持續觀察 / R·風險留意 /
D·美學前端參考 / G·Agent與Skill參考 / I·基礎設施工具 /
W·溝通與生活工具 / X·待分類

檔案類型：
filetype-yaml / markdown / image / spreadsheet / document / presentation /
pdf / code / config / archive / audio / video / unknown

資料確認狀態：
ai-proposed / human-confirmed / human-review / historical
```

---

# 附錄 C：AI 行動紀錄格式

```text
時間--智能體名稱--大語言模型--操作對象--動作--確認狀態

範例：
2026-09-03T13:40:00+09:00--Claude-Code--claude-fable-5--Ya-MiC/archify--remove-topic:env-cloudflare--human-confirmed
2026-09-03T14:00:00+09:00--Perplexity--research-agent--00-system-constitution.md--create-draft--pending-human-review
```

---

# 附錄 D：術語白話表

| 詞 | 白話意思 |
|---|---|
| Repository | GitHub 上的一個專案資料夾，能存程式、文件、版本歷史 |
| Topic | 貼在「整個倉庫」上的標籤 |
| Star | 收藏別人的倉庫 |
| Star List | 把 Star 放進收藏夾 |
| Issue | 一張具體問題/待辦/討論卡，不是分類工具 |
| Project | 多張 Issue 組成的任務看板，不是資產儀表盤 |
| OAuth | 用 GitHub/Google/Notion 帳號登入並選擇授權哪些資料 |
| PWA | 可安裝到桌面/手機主畫面的網頁 App |
| Tauri | 把網頁包成 Windows/macOS/Linux 桌面程式的開源工具 |
| OCR | 把照片/PDF 中的字辨識成文字/表格 |
| RAG | AI 回答前先到指定知識庫找資料並附來源，而不是只靠模型記憶 |
| Human Review | AI 不確定或不應決定時，交給人類確認 |
| Module Registry | 未來模組的正式登記簿：記錄需要、前提、風險與校對點，不等於丟著不管 |

---

> **創辦人確認入口**
>
> 請不要一次檢查全篇。先回答下列其中一種：
>
> - `A：同意本白皮書的大方向，下一步先修第 X 章。`
> - `B：不同意，核心錯誤是……`
> - `C：同意成為 v1.0，但下列模組維持 candidate，不得當成已實現：……`
>
> 在創辦人確認前，本文件不得被宣稱為公司正式承諾、產品功能清單、融資材料或審計軟體對外宣傳。
