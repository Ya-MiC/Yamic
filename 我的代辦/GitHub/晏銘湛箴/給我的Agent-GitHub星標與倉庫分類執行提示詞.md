# 任務提示詞：GitHub 星標分類 + 倉庫 Topics 打標籤

> 交辦對象：具有 GitHub 寫入權限的本機 Agent（Claude Code / Codex CLI / 其他已安裝 `gh` CLI 並登入的工具）
> 帳號：`Ya-MiC`
> 規則來源：Ya-MiC GitHub Portfolio OS Skill（v6）＋ Ya-MiC 人類主權第二大腦 OS Skill（第三部分、第四部分）
> 核心原則：**只准新增標籤／加星標／建立 List，絕對不准刪除任何東西、不准移除現有標籤或 List、不准取消任何現有星標**。若你判斷某個東西該刪除或該取消星標，必須停止並在最後的「待人類確認清單」列出，不得自己執行。

---

## 零、開始前必讀的安全規則

1. **不要 clone 任何倉庫**，也不要下載完整原始碼。只用 `gh repo view`、`gh api repos/{owner}/{repo}`、`gh repo view --json` 這類唯讀 metadata 指令。
2. **不要刪除、不要取消星標、不要移除任何現有 Topics 或 List**。只做「新增」。
3. 每一次寫入（加 Topics、加星標、建立/更新 List）都要在最後的執行報告裡，用這個格式記一行：

```text
時間--智能體名稱--大語言模型--操作對象
範例：2026-09-03T10:30:00+09:00--Claude-Code--claude-opus-4--zhanzhen-server(topics)
```

4. 遇到任何「不確定該歸哪一類」的情況，**不要亂猜**，先按你認為最接近的分類打上，同時在報告最後的「待人類確認清單」列出來，讓 Ya-MiC 自己回頭看一眼即可，不要因為猶豫而卡住整個流程。
5. 一個倉庫/星標**可以同時屬於多個分類**，不是單選——遇到「這個好像也符合另一類」的情況，兩個標籤都加，不要糾結選一個。

---

## 一、任務 A：把星標（Starred Repositories）分類進 List

### A.1 現有 List（已存在，不要重建，直接沿用）

```text
STUDY        （已有 13 個）
ADOPT候選    （已有 3 個）
```

### A.2 需要新建的 List（照這個代號＋名稱建立，一字不改）

```text
M·持續觀察
R·風險留意
D·美學前端參考
G·Agent與Skill參考
I·基礎設施工具
W·溝通與生活工具
X·待分類
```

### A.3 分類判斷邏輯（依序檢查，符合就加進對應 List，不排他）

對每一個 Starred repository，依序問自己以下問題，符合就加標：

```text
Q1. 這個倉庫是 Agent 框架、Skill 封裝格式、Prompt 工程、AI Agent 產品面板類？
    → 加入「G·Agent與Skill參考」
    （例如：codex-commander、archify、last30days-skill、arkvol-skill、
     argo、nie-grassroots-logic、wechat-radar 這類都算 G，
     即使 wechat-radar 主要功能是別的，只要它「本身是一個 Agent/面板產品」
     就也算 G——一個倉庫可以同時是 G 又是別的分類）

Q2. 這個倉庫的重點是視覺呈現、UI 設計、Dashboard、架構圖/知識圖譜？
    → 加入「D·美學前端參考」
    （例如：archify 本身同時是 G 也是 D，兩個都加）

Q3. 這個倉庫是研究資料、資料集、學術方法、量化/金融資料？
    → 加入「STUDY」（沿用既有 List，不新建）

Q4. 這個倉庫是網路、部署、Docker、DNS、伺服器、CLI 工具類？
    → 加入「I·基礎設施工具」

Q5. 這個倉庫是溝通方法、非暴力溝通、事實查核、生活類工具（非技術框架）？
    → 加入「W·溝通與生活工具」
    （例如：ayi-nonviolent-communication、FactReach 屬於這類）

Q6. 我已經明確想 fork 或整合進自己專案的？
    → 加入「ADOPT候選」（沿用既有 List）

Q7. 授權不明、看起來很久沒更新、有安全或合規疑慮，但還想留著觀察？
    → 加入「R·風險留意」

Q8. 不確定要不要用、但想繼續追蹤更新？
    → 加入「M·持續觀察」

Q9. 上面全部都不符合，或資訊不足判斷？
    → 加入「X·待分類」，不要用力猜，寧可放這裡等人類自己看
```

### A.4 執行方式（`gh` CLI 範例，依你的工具實際指令調整）

```bash
# 列出所有星標，取得 metadata
gh api /users/Ya-MiC/starred --paginate > starred_raw.json

# 對每個 repo 讀取 description、topics、language、pushed_at
gh repo view {owner}/{repo} --json description,repositoryTopics,primaryLanguage,pushedAt

# 加入 List（GitHub 網頁操作為主，若 CLI 不支援 List 寫入，
# 改成輸出一份「建議分類表」交給人類手動點擊）
```

> 如果你發現 `gh` CLI 或 GitHub API 目前不支援直接寫入 Star List（這是真實存在的限制），
> **不要卡住**，改成輸出一份 Markdown 表格：
>
> | 倉庫 | 建議 List（可多選） | 判斷理由 |
> |---|---|---|
>
> 讓 Ya-MiC 自己對著表格去網頁上點「Add to list」，這樣也算完成任務。

---

## 二、任務 B：把 Ya-MiC 自己的倉庫打上 Topics

### B.1 標籤前綴系統（固定四個前綴，不要自創新前綴）

```text
domain-   ai-agent | audit-saas | automation | data-research |
          device-setup | website | study | record | vision

role-     core-asset | business-engine | leverage-tool |
          infrastructure | learning-asset | record-asset

env-      windows | macos | linux | wsl | vps | docker |
          cloudflare | kubernetes

risk-     security-review | non-investment-advice | secret-review
```

### B.2 判斷邏輯

```text
Step 1　讀取倉庫的 description、README 開頭、目前語言、目前 Topics
Step 2　domain- 只選一個最主要的：
        - 明顯是審計/會計/財務 SaaS 產品 → domain-audit-saas
        - 明顯是 Agent/Skill/提示詞/AI 工作流 → domain-ai-agent
        - 明顯是自動化腳本/OCR/批次處理 → domain-automation
        - 明顯是資料分析/研究/學術 → domain-data-research
        - 明顯是系統設定/網路/VPS/DNS → domain-device-setup
        - 明顯是網站/前端展示頁 → domain-website
        - 明顯是課程作業/練習/學習用 → domain-study
        - 明顯是交接文件/歷史記錄/一次性資料 → domain-record
        - 明顯是還沒開始做、只有構想文件的 → domain-vision
        - 完全看不出來 → 不要打 domain-，改成在報告裡列入
          「待人類確認清單」，寧可空著也不要亂猜

Step 3　role- 選一個最主要的：
        - 是核心、不可替代的系統/總控 → role-core-asset
        - 直接產生收入/客戶的產品 → role-business-engine
        - 可被多專案重複使用的工具/模板 → role-leverage-tool
        - 底層部署/網路/安全支援 → role-infrastructure
        - 純學習用途 → role-learning-asset
        - 純保存歷史用途 → role-record-asset

Step 4　env- 可以多選，依實際使用的技術棧勾選
        （看 package.json、requirements.txt、Dockerfile、README 提到的部署方式）

Step 5　risk- 只在明確符合時才加：
        - 涉及金融/投資/量化結論的 → 加 non-investment-advice
        - 涉及網路安全工具、DNS、VPN、掃描器類 → 加 security-review
        - 有 .env 範例、疑似金鑰相關檔案的 → 加 secret-review
          （只是「加標籤提醒」，不是要你打開或讀取金鑰內容）
```

### B.3 已知的正確答案（這幾個不用重新判斷，直接套用）

```text
zhanzhen                         → domain-audit-saas role-core-asset env-docker
zhanzhen-server                  → domain-audit-saas role-business-engine env-docker risk-secret-review
zhanzhen-web                     → domain-website role-business-engine env-cloudflare
zhanzhen-handover                → domain-record role-record-asset
zhanzhen--audit-agent-blueprint  → domain-vision role-learning-asset risk-non-investment-advice
ya-mic-os                        → domain-ai-agent role-core-asset env-cloudflare
ya-mic-growth-log                → domain-record role-learning-asset
audit-os                         → domain-audit-saas role-business-engine
audit-os-mobile                  → domain-audit-saas role-leverage-tool
dsh                               → domain-ai-agent role-core-asset
hermes                            → domain-ai-agent role-leverage-tool
```

### B.4 其餘全部倉庫（約 50+ 個）處理方式

```text
1. 用 gh repo list Ya-MiC --limit 100 --json name,description,topics,pushedAt,visibility
   拉出完整清單
2. 排除上面 B.3 已經處理過的
3. 剩下的逐一套用 B.2 的判斷邏輯
4. 對每個倉庫執行（範例）：
   gh repo edit Ya-MiC/{repo} --add-topic domain-xxx --add-topic role-xxx
5. 完全看不懂用途、名稱像 123、-、q、warp- 這類的倉庫：
   不要打任何標籤，也不要刪除，直接列入「待人類確認清單」，
   維持 Ya-MiC 已有的 Human Review 慣例
```

---

## 三、最終輸出格式（任務結束時必須交這份報告）

```markdown
# GitHub 分類執行報告
時間：{執行時間}
執行者：{智能體名稱} / {大語言模型}

## 星標分類結果
- 已分類：{數量} 個
- 分類分布：STUDY({n}) / ADOPT候選({n}) / M·持續觀察({n}) / R·風險留意({n}) /
  D·美學前端參考({n}) / G·Agent與Skill參考({n}) / I·基礎設施工具({n}) /
  W·溝通與生活工具({n}) / X·待分類({n})
- 若 List 寫入 API 不支援，附上「建議分類表」供人工點擊

## 倉庫 Topics 打標結果
- 已打標：{數量} 個
- 逐一列出：{倉庫名} → {打上的 topics}

## 待人類確認清單
- {倉庫/星標名}：無法判斷的原因（不要猜，如實寫）

## 行動記錄（依 Skill 3 格式）
{時間}--{智能體名稱}--{模型}--{操作對象}
（每一筆寫入都要有一行）
```

---

## 四、給執行者的最後提醒

- 這是**輔助分類**，不是最終定論——Ya-MiC 本人保留最終修改權，你的分類只是草稿。
- 遇到任何「打了標籤但其實方向錯了」的擔心，不影響任務完成——標籤本來就可以事後改，錯了不是災難，**卡住不做才是問題**。
- 完成後不需要等待額外確認才能加 Topics/星標（這屬於 Gate 1／可逆的分類草案，不是 Gate 4 的破壞性操作），但絕對不能刪除、取消星標或移除現有標籤。
