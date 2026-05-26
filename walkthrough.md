# 變更導覽：Antigravity MAT 介紹投影片生成完成！

本導覽說明了我們如何運用 Python 自動化腳本，為您生成符合精密視覺標準的高質感說明會投影片，並完成首版 Git/GitHub 版本控管。

---

## 🎯 產出簡報下載與檢視

您的最新定稿投影片檔案已經生成完畢，並複製到 Artifacts 目錄下。請直接點擊下方連結下載與開啟：

👉 **[MAT_Antigravity_Introduction_v6.pptx (最終定稿版投影片)](file:///C:/Users/TK_Tsai/.gemini/antigravity/brain/cc4dc6c0-3eda-4eab-a71e-6bb7573eacb6/MAT_Antigravity_Introduction_v6.pptx)**

---

## 🎓 MAT 同事專屬：兩大實戰練習課 (Lab Exercises) 講義

為了讓同仁在說明會後能立刻動手玩、親自感受 **Antigravity** 的強大威力，我們特別設計了兩大「實戰練習」，並為大家準備好可以直接複製貼上的 **黃金開發 Prompt**！

---

### 📘 練習一：自建會議紀錄與 Outlook 郵件草稿串接 Skill
*   **練習目標**：同仁將親自建立一個名為 `meeting-minutes` 的自訂技能，實現多媒體資訊擷取與 Outlook 草稿自動化寫入。
*   **功能規範**：
    1.  **關鍵擷取**：從會議錄音 (MP3)、錄影 (MP4) 檔或會議逐字稿文字檔中，精準擷取決議事項與 Action Items，並整理成繁體中文結構化的會議紀錄 Markdown。
    2.  **串接 Outlook**：自動尋找 Microsoft Outlook 中對應時間或主題的會議，將該會議紀錄自動寫入到該會議的郵件草稿 (Email Draft) 中！

#### 📝 同仁開發用的黃金 Prompt (直接複製貼給 Antigravity)：
```markdown
我想開發一個名為 `meeting-minutes` 的自訂 Skill。
請幫我建立對應 of SKILL.md 技能指南與輔助的 Python CLI 腳本。

【核心功能需求】：
1. 支援讀取會議逐字稿文字檔、MP3 音訊檔案、以及 MP4 影片檔案。從中精準擷取會議關鍵資訊（包含：會議主題、時間、出席者、核心決議事項、待辦 Action Items），並自動生成結構化且美觀的繁體中文會議紀錄 Markdown 報告。
2. 整合微軟 Outlook 功能，能在 Outlook 郵件系統中尋找對應時間或特定主題的會議，並自動將剛生成的會議紀錄寫入到該會議的「郵件草稿 (Email Draft)」中，方便使用者確認後一鍵發送給所有出席同仁。

【開發原則】：
- 請先為我寫出完整的「實作計畫書 (Implementation Plan)」，待我確認核准後，再使用 uv 與 .venv 虛擬環境開始開發，絕不弄髒本機 Base 環境！
```

#### 🚀 開發與操作步驟引導：
1.  **新建工作區**：在 `scratch/` 下建立一個子目錄，例如 `my_meeting_minutes_skill`，並在 VS Code 中開啟它。
2.  **投遞 Prompt**：將上述 Prompt 貼入 Antigravity 聊天框中。
3.  **確認計畫**：審查 AI 產出的 `implementation_plan.md`，輸入「同意」。
4.  **自動開發**：AI 會自動使用 `uv` 建立虛擬環境，安裝需要的套件（如用 Python 串接 Outlook API 或文字處理庫），自律完成開發。

---

### 📙 練習二：MP4 轉 MP3 命令行小工具 (規劃與開發)
*   **練習目標**：讓同仁親自體驗 Antigravity 的 `/brainstorm`（動手前先想清楚）流程，學習如何與 AI 進行高品質的需求對齊，並完成小工具開發。
*   **實戰步驟與 Prompt 引導**：

#### 🚀 步驟 1：啟動規劃 ── 對著 Antigravity 輸入：
```bash
/brainstorm 我想開發一個 mp4 轉 mp3 的簡單命令列小工具
```

#### 🚀 步驟 2：自適應對話對齊：
*   AI 啟動 brainstorm 機制後，會主動詢問您溝通模式。請選擇 **「🟢 小白模式」** 或 **「🟡 半技術模式」**。
*   AI 會列出它對這個小工具的假設（例如：支援單檔轉換、是否需要支援批次轉換、套件相依性等），並與您對齊理解。

#### 🚀 步驟 3：核准並自動實作：
*   對齊理解後，AI 會自動在 `plans/` 資料夾下為您生成一份精密的實作計劃書（Markdown）。
*   您只要對它說：**「同意，請開始執行！」**
*   Antigravity 就會自動初始化 `uv` 虛擬環境，安裝相依影音套件（如 `moviepy`），自動寫出完整的 `convert.py` 工具並跑通測試，最後產出 walkthrough 成果導覽！

---

## 📦 功能分發指南：哪些是內建？哪些需要分享檔案？

當您向 MAT 同事介紹 these 強大功能時，請務必說明哪些是 Antigravity 原生自帶的，哪些需要透過您分享檔案給他們：

### 1. 🌐 原生自帶功能 (開箱即用，免分享檔案)
這兩項是 Antigravity 核心引擎內建的斜線指令與功能。同事只要安裝並登入好 Antigravity，**直接在對話框輸入即可使用，不需要任何額外檔案**：
*   **`/goal` 指令** ── 啟動深度長跑任務模式，讓 AI 發揮極致耐心直到目標完全達成為止。
*   **`/browser` 指令** ── 啟動線上瀏覽功能，引導 AI 上網搜尋最新文獻與 API 官方文檔。

### 2. 🛠️ 自訂擴充 Skill (需要由您分享檔案，貼到指定位置)
這兩者是我們為 Antigravity 特別編寫與擴充的 **「自訂技能 (Skills)」**。同仁的電腦預設**沒有**這兩個功能。您必須將您電腦中的 **Skill 資料夾** 分享給他們，並請他們放到對應路徑下，方可加載生效：
*   **`/brainstorm`** (引導式需求釐清與計劃書生成)
*   **`workflow-skill-creator`** (將成功工作流自動打包成可複用 Skill)

#### 📂 您需要分享給同事的檔案路徑 (已為您備份在專案下！)
為了讓您分發最方便，我已經把這兩個擴充 Skill 的完整檔案複製備份到本專案的 `skills/` 資料夾下了！您只需要打包分享：
1.  **`brainstorm` 技能資料夾**：
    👉 本專案中的 `skills/brainstorm/` 資料夾
2.  **`workflow-skill-creator` 技能資料夾**：
    👉 本專案中的 `skills/workflow_skill_creator/` 資料夾

#### 📥 同事收到後的安裝步驟
請同事將您分享的這兩個資料夾解壓縮後，複製貼到他們自己電腦的 **全域自訂技能目錄** 下：
👉 **`C:\Users\<同事Username>\.gemini\config\skills\`**

---

## 💡 Antigravity 的全域協作規範 (Global Rules) 與設定方法

為了讓您的 Antigravity 虛擬隊友與您的開發習慣完美同頻，您為系統設定了極起嚴謹的 **Global Rules**。以下是這些 Rules 的核心內容與設定教學，這非常適合直接分享給 MAT 的同事：

### 1. 您的全域設定 Prompt (Global Rules) 原始內容
```markdown
# 個人偏好（全域）
 
- 預設語言：繁體中文（請以繁體中文回應自然語言與文件內容），包括你自己的思考過程(thinking process)，都使用繁體中文和自己交談
- 文件（README、CLAUDE.md、commit message 等）預設使用繁體中文
- 程式碼本體保留原始語言，但註解、說明與 docstring 請使用繁體中文
- 如果要使用python開發程式，一定要使用 uv, .venv 建立環境，千萬不要用到base及單獨使用pip，不要弄髒我的環境
- 自動產生 git commit messages/comments時，一律使用繁體中文台灣用語
- Agent 產生的 implementation.plan*, task.md*, walkthrought.md*，全部用繁體中文台灣用語
作業系統為windows 作業環境
# 版本控管
-第一版本使用gh建立repo並上傳
如果分析功能異動太大，需要先建立分支。任務完成後再詢問是否合併回主分支
```

### 2. 如何讓團隊同事的 Antigravity 套用這個 Rules？(設定方法)

有以下三種主要方式可以讓大家的 Antigravity 助手完全遵守這些自訂規範：

#### 🟢 方法 A ── 專案級自訂 `GEMINI.md` (🌟 最推薦，適合團隊共用)
*   **做法**：在專案的根目錄下建立一個名為 `GEMINI.md` 的 Markdown 檔案（系統亦相容讀取 `CLAUDE.md`），將上述 Rules 貼入其中。
*   **原理**：**Antigravity** 在開啟並解析工作區（Workspace）時，會**第一時間自動讀取並 100% 遵守** `GEMINI.md` 裡的規範。
*   **優點**：極利於團隊協作！同事只要 clone 這份專案，大家的 Antigravity 行為就會完全一致，不需個人做任何額外設定！
*   *(本專案已建立 [GEMINI.md 範本](file:///C:/Users/TK_Tsai/.gemini/antigravity/scratch/antigravity_mat_presentation/GEMINI.md) 作為 Demo 的實物教材。)*

#### 🟡 方法 B ── 全域級自訂 `GEMINI.md` (🌟 跨專案一勞永逸！)
*   **做法**：請同事直接在個人使用者家目錄的隱藏設定資料夾下，建立以下全域設定檔：
    👉 **`C:\Users\<Username>\.gemini\GEMINI.md`**
*   **原理**：這是 Antigravity 在您的 Windows 電腦中最官方、最純正的**全域自訂規則設定路徑**。只要在此處放置您的 Global Rules，此後您在電腦上任何目錄開啟 Antigravity 協作，AI 都會自動在背景讀取套用，完全不需要重複設定！

#### 🔴 方法 C ── 系統全域 User Rules 介面設定
*   **做法**：請同事打開 **Antigravity 客戶端設定介面**，在 **「User Rules」** 或 **「Custom Instructions」** 欄位中，直接將上述 Prompt 貼入儲存，即可跨專案自動套用您的個人開發偏好。

---

## 🎨 簡報視覺風格與實作成果

本投影片嚴格遵守您所指定的精密視覺規範：

*   **投影片尺寸**：`13.33" × 7.50"` (寬螢幕 16:9 比例)。
*   **字型設計**：標題使用 `Abadi`，內文與細節使用 `Arial` 與 `微軟正黑體`，大小配置得體、清晰易讀。
*   **主題色系**：
    *   主色填充與強調：`#125C69` (松石綠)
    *   卡片底色 (Cards)：`#DBEFEF` (淺松石藍)
    *   主要文字色：`#334155` (暗石灰藍)
    *   第一頁封面：採用暗底 `#0A1628`，營造大氣、科技感的 WOW 第一印象。
    *   其餘頁面：清爽的白底，搭配精緻元素。
*   **精準坐標與裝飾**：
    *   **Accent Bar**：每頁 (0.7", 0.5") 位置皆精確畫有 `0.08" × 0.52"` 的松石綠裝飾條。
    *   **Section Pill**：每頁 (0.6", 1.3") 位置皆精確畫有 `3.70" × 0.42"` 的圓角藥丸形單元標籤，文字在內部垂直居中，美觀大方。

---

## 📂 投影片 10 大頁面佈局一覽

1.  **Slide 1：封面 (暗底)** ─ 標題 `Antigravity` 配合副標題，帶來精緻強烈的視覺衝擊。
2.  **Slide 2：什麼是 Antigravity？ (雙卡片排版)** ─ 介紹 Agentic AI 的自主開發體驗與「實作計畫/任務清單/變更導覽」三大機制。
3.  **Slide 3：環境設定極速上手 (三橫欄卡片)** ─ 介紹工作區、Git 版控，並強烈強調「使用 `uv` 與 `.venv` 防止環境污染」。
4.  **Slide 4：自訂協作規範：Global Rules (雙卡片排版)** ─ 介紹 MAT 團隊全域開發偏好，並完整提供最純正的全域 `.gemini/GEMINI.md` 與專案級 `GEMINI.md` 設定方法。
5.  **Slide 5：擴充功能分發與安裝指南 (雙卡片排版)** ─ 🌟 **[位置調整]** 移到規則說明之後，介紹自訂 Skill 的備份與貼上路徑。
6.  **Slide 6：5分鐘現場 Demo 流程 (步進流程)** ─ 以 4 步驟小卡片串接，清晰呈現從對齊需求到產出 Walkthrough 的 Demo 動線。
7.  **Slide 7：動手前先想清楚：/brainstorm (對稱卡片)** ─ 深度介紹 **🟢 小白模式** (無門檻、成果導向) 與 **🔴 工程師模式** 的自適應彈性。
8.  **Slide 8：打造 MAT 專屬工具庫 (矩陣排版)** ─ 介紹 `workflow-skill-creator` 如何將經驗提煉成 Skill，並介紹內建的 `Rate Limiting` 與 `File-lock` 防護。
9.  **Slide 9：MAT 同事專屬實戰練習課 (雙卡片排版)** ─ 自建會議紀錄與 Outlook 郵件草稿串接 Skill、MP4 轉 MP3 命令行小工具開發實戰。
10. **Slide 10：協作最佳實踐 (三欄卡片)** ─ 指導同事善用 `/goal`、`/browser` 指令，以及台灣用語版控習慣。

---

## 🛠️ 技術實作與環境安全 (防污染原則)

*   **專案路徑**：`C:\Users\TK_Tsai\.gemini\antigravity\scratch\antigravity_mat_presentation`
*   **虛擬環境隔離**：專案透過 **`uv` 與 `.venv`** 初始化。`python-pptx` 等相依套件全數安裝在該專屬虛擬環境中，保證主機 Base 環境完全不被弄髒。
*   **自動化版本控管 (gh CLI)**：
    *   使用 `git` 進行版控，並自動使用台灣繁體中文撰寫 Git commit message (`feat: 徹底正名規則檔為 GEMINI.md，新增全域設定路徑，並發布 v4 定稿投影片`)。
    *   使用 **GitHub CLI (`gh`)** 在遠端自動建立公開 Repo並成功推送代碼。
    *   遠端儲存庫連結：[mat-antigravity-introduction (GitHub)](https://github.com/qscf11-png/mat-antigravity-introduction)
