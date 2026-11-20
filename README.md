## 你好，我是 Arlen

業務管理背景，從一線工作的痛點出發，用 AI 做出**每月實際在用、而且能驗證對錯**的工具。

逢甲電機系畢業，目前是教育產業的經營管理副理，帶師資、教務、業務 9–12 人。超過一年來，把部門的重複性工作做成 AI 工具與 Python 自動化，再進一步學習 RAG、Tool Use、MCP 與模型評估，把做法整理成下面的作品。

### 我做事的方式

- **從真實問題開始**：每個工具都來自部門實際卡住的地方，用節省的時間衡量成效
- **不直接相信 AI 的輸出**：重要規則由程式再檢查一次，就像月報要三表勾稽；查不到就標示「待確認」，不讓 AI 猜
- **用數字改進**：每個專案都有評估題組或自動測試，改一版、量一次

### 團隊導入

| 工具 | 使用者 | 使用期間 | 成效 |
| --- | --- | --- | --- |
| 每月業績報表自動分類 | 3 位主管 | 1 年 | 第一次使用就節省時間，至今沒有出現問題 |
| 留學選校顧問 Agent | 6 位留學顧問 | 8 個月 | 顧問直接產出選校表與學生討論，節省整理時間；資料錯誤率低，與人工整理相當 |

導入的做法是**自己先實際使用，確認沒有缺失後才推廣**，讓同事第一次用就能信任工具。

### 作品

| 專案 | 內容 | 成果 |
| --- | --- | --- |
| [monthly-revenue-classifier](https://github.com/chunyang130/monthly-revenue-classifier) | Python 自動分類每月業績報表，三表金額自動勾稽 | 每月作業 8 小時 → 20 分鐘，回測準確率約 99%；3 位主管使用中 |
| [study-abroad-school-selection-agent](https://github.com/chunyang130/study-abroad-school-selection-agent) | 留學選校 Claude Agent Skill，只採官網等首要來源防止幻覺 | 選校表 2 小時 → 10 分鐘；試作僅 1 筆錯誤，靠每欄附的官網連結當場發現；6 位顧問使用中 |
| [consultation-notes-structurer](https://github.com/chunyang130/consultation-notes-structurer) | Claude API＋Tool Use 把口語諮詢摘要轉成固定欄位，存入 SQLite 產生追蹤報表 | 三輪真實測試：狀態判斷 7/8 → 8/8，跟進日期 3/4 → 4/4 |
| [course-qa-rag](https://github.com/chunyang130/course-qa-rag) | 課程問答 RAG：BM25 檢索、強制引用、程式驗證；提供 HTTP API 與問答網頁，以 Docker 容器化部署到 Google Cloud Run | 檢索與答對率 13/14 → 14/14，資料沒有的問題 3/3 正確拒答；[**線上示範**](https://course-qa-rag-799013895800.asia-east1.run.app) |
| [course-kb-mcp](https://github.com/chunyang130/course-kb-mcp) | 不用 SDK、自行實作 MCP 協定，讓 Claude Desktop 查詢課程文件 | 18 項協定測試，已實際接上 Claude Desktop 運作 |
| [model-benchmark](https://github.com/chunyang130/model-benchmark) | 同一份考卷比較 Claude、Gemini 與地端開源模型的品質、速度、成本 | 此任務 Haiku 全對、每千題 0.21 美元；貴 20 倍的 Sonnet 沒有更好 |

所有專案都使用虛構或去識別化的資料，並以 GitHub Actions 自動測試。程式由我與 Claude Code 協作完成；需求、業務規則、驗證方式與取捨由我決定。

### 技術

Python · SQL（SQLite） · Claude API · Gemini API · Ollama · RAG · Tool Use · MCP · Prompt 設計 · LLM 評估 · Docker · Google Cloud Run · GitHub Actions
