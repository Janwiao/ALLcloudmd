# 雲端儲存與分享使用指南

> 更新日期：2026-10-06  
> 本文以 **個人使用、團隊使用、頻繁修改、公開分享、大容量收藏** 五個面向，快速比較常見雲端服務。  
> 評分為用途定位分析，不是服務商官方評分；實際方案、價格與流量限制以官方最新資訊為準。

---

## 先看結論

| 服務 | 個人使用 | 團隊使用 | 頻繁修改 | 公開分享 | 大容量收藏 | 最適合做什麼 |
|---|---:|---:|---:|---:|---:|---|
| **Google Drive** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ | 文件、協作、日常跨裝置 |
| **pCloud** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 長期收藏、冷資料、雲端總倉庫 |
| **Dropbox** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | 多裝置同步、團隊工作 |
| **MEGA Free** | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | 中轉、大檔臨時分享 |
| **MediaFire Free** | ⭐⭐ | ⭐ | ⭐ | ⭐⭐⭐⭐ | ⭐ | 免費公開下載 |
| **GitHub（Repo / Releases）** | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐* | ⭐⭐⭐⭐⭐ | ⭐ | 程式開發、版本控制、軟體發布 |
| **Cloudflare R2** | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 網站、Client、Patch、大流量下載 |

> * GitHub 的「頻繁修改 5★」是指 **Source Code + Git 工作流**，不是把 Releases 當 Dropbox 使用。

---


## 互動式需求推薦器

網站版提供快速需求篩選，可複選：

- 個人日常
- 團隊協作
- 頻繁修改一般檔案
- 大容量收藏
- 公開分享
- 程式碼開發
- 軟體／工具發布
- Client / Patch 大量下載

系統會依各服務對每個情境的 **1～5 分適配度**，將所選需求取平均並換算成 **0～100 推薦指數**，即時列出前三名與完整排名。

> 推薦指數是用途適配分析，不是速度實測、官方評分，也不直接代表價格 CP 值。

---


## 雲端名詞字典

### 先記住：Sync 不等於 Backup

- **Sync（同步）**：讓本機與雲端保持一致。通常是雙向，任一端修改都可能反映到另一端；刪除也可能被同步。
- **Backup（備份）**：核心是保留可恢復副本。不同服務對刪除、版本歷史、保留時間的規則不同，不能只看名字判斷。
- **Online-only（僅線上）**：檔案看得到，但完整內容主要在雲端；真正開啟時才下載。
- **Available offline（離線可用）**：雲端與本機都有完整副本，沒有網路也能使用。
- **Cache（快取）**：為加速存取而暫存在本機的資料，不應視為正式備份。
- **Shared Link / Public Link**：給別人下載或存取的分享網址。
- **Transfer Quota / Bandwidth**：一定時間內能傳多少資料的額度。
- **Version History / Rewind**：保留舊版本或讓檔案／帳戶回到先前狀態。

### Google Drive

| 名詞 | 白話意思 |
|---|---|
| **Drive for desktop** | Google 的 Windows / macOS 桌面程式 |
| **Stream files** | 檔案主要在雲端，本機按需下載與快取，省硬碟 |
| **Mirror files** | 雲端與本機都保留完整副本，永遠可離線，但占硬碟 |
| **Shared drives** | Google Workspace 的團隊共用空間，資料屬於團隊而不是單一成員 |

Google 官方指出，高頻寫入、影片剪輯、高解析圖片工作通常 Mirror 會更快。

### pCloud

| 名詞 | 白話意思 |
|---|---|
| **pCloud Drive** | 虛擬雲端磁碟；主要資料在雲端，需要才抓 |
| **pCloud Sync** | 指定本機資料夾與 pCloud 資料夾做雙向同步 |
| **pCloud Backup** | 持續將指定本機資料夾更新到 pCloud；仍需注意刪除與版本保留規則 |
| **Crypto Folder** | pCloud 的額外加密資料區域 |

### Dropbox

| 名詞 | 白話意思 |
|---|---|
| **Online-only** | 只存在雲端，開啟時下載 |
| **Available offline** | 本機也保留完整副本 |
| **Selective Sync** | 決定哪些 Dropbox 資料夾要出現在這台電腦 |
| **File Request** | 建立收件入口，讓別人上傳檔案給你 |

### MEGA

| 名詞 | 白話意思 |
|---|---|
| **Transfer quota** | 下載／串流會消耗的傳輸額度 |
| **Sync** | 本機與 MEGA 資料夾同步 |
| **Backup** | 偏向保護本機資料夾的備份工作流，實際保留規則仍看服務設定 |

### GitHub

| 名詞 | 白話意思 |
|---|---|
| **Repository / Repo** | Git 專案儲存庫 |
| **Commit** | 一次版本變更紀錄 |
| **Branch** | 獨立開發線 |
| **Pull Request / PR** | 提出合併變更並進行 Review |
| **Release** | 正式版本發布頁 |
| **Asset** | Release 底下的 ZIP / EXE / Installer 附件 |
| **Git LFS** | Git Large File Storage，大型檔案的專門儲存機制 |

### Cloudflare R2

| 名詞 | 白話意思 |
|---|---|
| **Bucket** | 存放 Objects 的最上層容器 |
| **Object** | 真正儲存的一份檔案／資料 |
| **Key** | Object 的唯一名稱；畫面中的資料夾多半只是 prefix 視覺分組 |
| **Egress** | 從 R2 傳到 Internet 的出站流量 |
| **Public Bucket** | 允許 Internet 公開讀取的 Bucket |
| **Presigned URL** | 有期限、有限權限的私人 Object 存取網址 |
| **S3-compatible** | 可使用大量 S3 SDK / CLI / 工具 |
| **Storage Class** | Standard / Infrequent Access 等儲存類別 |
| **Class A / B Operations** | R2 API 操作的計費分類 |

### MediaFire

- **Ad-supported download**：免費分享時，下載者透過有廣告的 MediaFire 頁面取得檔案。

---


## 方案與價格

> 更新：2026-10-06。不同國家、稅金、付款方式與促銷會造成差異；以下保留各服務原始計價幣別，實際結帳頁優先。

### 計費模式快速看

| 服務 | 主要計費方式 |
|---|---|
| Google One | 月 / 年訂閱 |
| pCloud | 月 / 年訂閱 + Lifetime 一次買斷 |
| Dropbox | 個人訂閱；團隊方案多為每使用者計價 |
| MEGA | 月 / 年訂閱 |
| MediaFire | 免費 + 月 / 年訂閱 |
| GitHub | Free / Team / Enterprise，每人計價 + 額外用量 |
| Cloudflare R2 | 儲存量 + API Operations 按量計費 |

### Google One / Google Drive

| 方案 | 容量 | 公開價格參考 |
|---|---:|---:|
| 免費 | 15GB | US$0 |
| Basic | 100GB | US$1.99 / 月 |
| Standard | 200GB | 依地區 / 帳戶方案頁顯示 |
| Premium | 2TB | US$9.99 / 月（全球公開參考） |

> Google One 年繳方案官方標示最高可省約 16%；台灣與其他地區實際價格以帳戶內方案頁為準。

### pCloud

**常態價**

| 容量 | 年繳 | Lifetime |
|---|---:|---:|
| 500GB | US$49.99 / 年 | US$219 |
| 2TB | US$99.99 / 年 | US$499 |
| 10TB | US$299.99 / 年 | US$1,499 |

**2026 中秋活動（至 2026/10/7）**

| 容量 | Lifetime 活動價 | 特典 |
|---|---:|---|
| 1TB | US$279 | pCloud Encryption |
| 2TB | US$379 | pCloud Encryption |
| 10TB | US$1,099 | pCloud Encryption |

### Dropbox

| 方案 | 容量 | 價格 |
|---|---:|---:|
| Basic | 2GB | 免費 |
| Plus | 2TB | US$9.99 / 月 |
| Standard | 團隊至少 3TB | US$15 / 使用者 / 月 |
| Advanced | 團隊起始 15TB | US$24 / 使用者 / 月 |

> 月繳 / 年繳切換會影響 Dropbox 頁面顯示價格。

### MEGA

> MEGA 2026 年方案容量曾調整，並會受地區 / VAT 影響；以下以 2026 公開價格頁快照為參考，結帳頁優先。

| 方案 | 容量 | 月費參考 |
|---|---:|---:|
| Free | 20GB | €0 |
| Pro Lite | 約 750GB | 約 €4.99 / 月 |
| Pro I | 3TB | €9.99 / 月 |
| Pro II | 10TB | €19.99 / 月 |
| Pro III | 20TB | €29.99 / 月 |

### MediaFire

| 方案 | 容量 | 價格 |
|---|---:|---:|
| Basic | 10GB | 免費 / 廣告支援下載 |
| Pro | 1TB | US$5.83 / 月（年繳折算） |
| Pro 月繳 | 1TB | 約 US$9.99 / 月，促銷可能變動 |
| Ultra | 100GB | US$10 / 月 |

### GitHub

| 方案 | 價格 | 定位 |
|---|---:|---|
| Free | US$0 | 個人 / 組織基本功能 |
| Team | US$4 / 使用者 / 月 | 團隊協作 |
| Enterprise | US$21 / 使用者 / 月起 | 企業治理 / 合規 |

> Actions、Codespaces、Packages、Git LFS 等超出內含額度時可能另外計費。

### Cloudflare R2

| 項目 | 價格 |
|---|---:|
| Standard Storage | US$0.015 / GB-month |
| Infrequent Access Storage | US$0.01 / GB-month |
| IA Retrieval | US$0.01 / GB |
| Class A Operations | US$4.50 / 百萬次 |
| Class B Operations | US$0.36 / 百萬次 |
| Internet Egress | 免費 |

Standard 免費層每月包含：10GB-month Storage、100 萬次 Class A、1,000 萬次 Class B。

只算 Standard Storage、扣掉 10GB 免費額度時：

- 1TB：約 US$14.85 / 月
- 5TB：約 US$74.85 / 月
- 10TB：約 US$149.85 / 月

> 上述未計入 Operations。

---

## 1. 五個評分面向怎麼看？

### 個人使用
自己上傳、下載、跨裝置、保存與管理資料的方便程度。

### 團隊使用
多人共同使用、權限管理、共同編輯、版本追蹤與協作工作流。

### 頻繁修改
同一批工作檔每天反覆修改、儲存、同步與跨裝置更新時的適合程度。

### 公開分享
把連結貼到 Discord、論壇、網站，讓其他人下載檔案時的適合程度。

### 大容量收藏
數 TB 冷資料、歷史版本、素材、壓縮檔等長期保存的成本與使用體驗。

---

## 2. 容量和流量不是同一件事

| 名稱 | 白話解釋 |
|---|---|
| **Storage** | 倉庫能放多少東西 |
| **Upload** | 搬多少資料進雲端 |
| **Download** | 自己從雲端拿回多少資料 |
| **Shared Traffic** | 別人透過分享連結拿走多少資料 |
| **Egress** | 雲端送到 Internet 的出站流量 |
| **Operations** | 讀、寫、列出物件等操作次數 |

例如只存一個 **10GB** 檔案：

- Storage：10GB
- 自己下載 3 次：30GB 傳輸
- 1,000 人各下載一次：約 10TB 分享／出站流量

> **Storage ≠ Traffic。容量很大，不代表公開分享頻寬也很大。**

---

# 3. Google Drive

**個人：⭐⭐⭐⭐⭐　團隊：⭐⭐⭐⭐⭐　頻繁修改：⭐⭐⭐⭐⭐　公開分享：⭐⭐　收藏：⭐⭐⭐**

### 優點
- Google Docs / Sheets / Slides 協作非常成熟
- Drive for desktop 有 Stream / Mirror
- 搜尋、預覽、手機與電腦整合完整
- 很適合多人文件與一般工作資料夾
- Mirror 模式適合需要大量本機讀寫的工作檔

### 缺點
- 數 TB 長期收藏成本通常不是最漂亮
- 熱門公開檔案可能被暫時限流
- 不適合當大型 Installer / Client 公開下載站

### 最適合
- 文件、PDF、試算表
- 團隊共同編輯
- 日常工作資料
- 多裝置使用
- 頻繁修改的一般工作檔

官方：
- https://support.google.com/drive/
- https://support.google.com/a/users/answer/7338880

---

# 4. pCloud

**個人：⭐⭐⭐⭐⭐　團隊：⭐⭐⭐　頻繁修改：⭐⭐⭐⭐　公開分享：⭐⭐⭐　收藏：⭐⭐⭐⭐⭐**

### 優點
- Lifetime 與大容量收藏是主要特色
- pCloud Drive 可做虛擬磁碟
- pCloud Sync 可做本機雙向同步
- 很適合冷資料、歷史版本、素材與壓縮封存
- 不需要把整個雲端完整占用本機空間

### 缺點
- 團隊協作能力不如 Google Drive / Dropbox
- 虛擬磁碟不是高速 SSD
- 公開分享有 Shared Link Traffic
- 大量持續變動的小檔案，不是它最強的使用情境

### 最適合
- 個人大容量總倉庫
- 歷史資料
- 冷資料
- 素材與壓縮檔
- 一般工作資料夾同步（使用 Sync）

2026 常見個人方案流量：

| 方案 | Storage | Shared Link Traffic | Upload Traffic |
|---|---:|---:|---:|
| Basic | 最多 10GB | 50GB / 月 | 約為容量 2 倍 / 30 日 |
| Premium | 500GB | 1TB / 月 | 最高 1TB / 30 日 |
| Premium Plus | 2TB | 4TB / 月 | 最高 4TB / 30 日 |
| Ultra | 10TB | 20TB / 月 | 最高 4TB / 30 日 |

官方：
- https://help.pcloud.com/article/plan-details
- https://help.pcloud.com/article/shared-link-traffic

---

# 5. Dropbox

**個人：⭐⭐⭐⭐⭐　團隊：⭐⭐⭐⭐⭐　頻繁修改：⭐⭐⭐⭐⭐　公開分享：⭐⭐⭐⭐　收藏：⭐⭐⭐**

### 優點
- 多裝置同步非常成熟
- Online-only / Available offline 清楚好用
- 團隊資料夾與協作流程成熟
- 對頻繁修改、儲存、跨裝置同步的工作資料很強

### 缺點
- 長期大容量冷資料通常不是價格優勢
- 公開分享仍有每日頻寬限制
- 如果只是「放多年不動」，它的同步優勢用不到

### 最適合
- 工作資料
- 多台電腦
- 團隊專案
- 頻繁修改的資料夾
- 多人協作

分享頻寬：

| 方案 | 分享頻寬 |
|---|---:|
| Basic | 20GB / 日 |
| Plus / Family / Professional / Essentials / Standard / Business | 1TB / 日 |
| Advanced / Business Plus / Enterprise | 4TB / 日 |

官方：
- https://help.dropbox.com/share/banned-links
- https://help.dropbox.com/sync/make-files-online-only

---

# 6. MEGA Free

**個人：⭐⭐⭐　團隊：⭐⭐　頻繁修改：⭐⭐⭐　公開分享：⭐⭐　收藏：⭐⭐**

### 優點
- 隱私與加密定位清楚
- 大型檔案中轉方便
- 桌面與網頁工具完整

### 缺點
- Free Transfer quota 會影響大型下載
- 免費方案不適合長期大量團隊使用
- 不適合熱門公開下載站

### 最適合
- 中轉
- 接收資料
- 臨時大檔
- 私人分享

官方：
- https://mega.io/pricing
- https://help.mega.io/

---

# 7. MediaFire Free

**個人：⭐⭐　團隊：⭐　頻繁修改：⭐　公開分享：⭐⭐⭐⭐　收藏：⭐**

### 優點
- 免費公開分享簡單
- 適合 MOD、補丁、小工具、ZIP
- Ad-supported download 模式對公開分享友善

### 缺點
- 免費容量小
- 不適合多人工作
- 不適合頻繁同步
- 不適合數 TB 私人收藏

### 最適合
- 免費公開下載
- 小型檔案分享

官方：
- https://www.mediafire.com/

---

# 8. GitHub（Repository / Releases）

**個人：⭐⭐⭐　團隊：⭐⭐⭐⭐⭐　頻繁修改：⭐⭐⭐⭐⭐*　公開分享：⭐⭐⭐⭐⭐　收藏：⭐**

> * 頻繁修改 5★ 僅限 **程式碼、文字檔與 Git 工作流**。

### Repository 最適合
- Source Code
- Markdown
- YAML / JSON
- 網站原始碼
- 多人開發
- Branch / PR / Review

### Releases 最適合
- 工具
- 編譯成品
- Installer
- 版本更新包

GitHub Releases 目前官方說明：
- 每個 Release 最多 1,000 個 assets
- 每個 asset 小於 2 GiB
- Release 總大小沒有上限
- Bandwidth usage 沒有上限

### 不適合
- 把大型 Client、ISO、素材庫當一般雲端硬碟同步
- 用 Releases 取代 Dropbox

官方：
- https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases

---

# 9. Cloudflare R2

**個人：⭐⭐⭐　團隊：⭐⭐⭐　頻繁修改：⭐⭐　公開分享：⭐⭐⭐⭐⭐　收藏：⭐⭐⭐**

### 優點
- Object Storage
- Internet Egress 免費
- 適合網站、Client、Patch、圖片與大型公開檔案
- API / Worker / CDN 整合彈性高

### 缺點
- 不是一般使用者同步硬碟
- 沒有 Google Drive / Dropbox 那種資料夾協作體驗
- 頻繁修改小檔案會牽涉大量 Operations
- 需要管理 Bucket、權限與 API

Standard Storage 常見價格：
- Storage：US$0.015 / GB-month
- Class A：US$4.50 / 百萬次
- Class B：US$0.36 / 百萬次
- Internet Egress：Free

官方：
- https://developers.cloudflare.com/r2/

---

# 10. 頻繁修改到底選誰？

| 情境 | Google Drive | Dropbox | pCloud | GitHub |
|---|---:|---:|---:|---:|
| Office / PDF / 一般文件 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐ |
| PSD / 圖片 / 一般工作資料夾 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐ |
| 多台電腦反覆同步 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐ |
| 多人共同編輯文件 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ |
| Source Code | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐⭐⭐ |
| 冷資料、歷史版本 | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐ |

### 簡單理解
- **Dropbox**：檔案同步專長
- **Google Drive**：文件協作 + 本機同步都很強
- **pCloud**：收藏最強，一般 Sync 也能做
- **GitHub**：程式碼的頻繁修改最強，但它不是一般雲端硬碟

---

# 11. 最後怎麼選？

### 個人使用
| 需求 | 推薦 |
|---|---|
| 文件、照片、日常資料 | **Google Drive** |
| 多裝置高頻同步 | **Dropbox / Google Drive** |
| 大容量長期收藏 | **pCloud** |
| 臨時中轉 | **MEGA** |

### 團隊使用
| 需求 | 推薦 |
|---|---|
| 文件協作 | **Google Drive** |
| 團隊檔案同步 | **Dropbox** |
| 程式開發 | **GitHub** |
| 網站 / App Object Storage | **Cloudflare R2** |

### 公開分享
| 需求 | 推薦 |
|---|---|
| 工具 / 程式版本 | **GitHub Releases** |
| 免費分享小檔 | **MediaFire** |
| Client / Patch / 網站大型下載 | **Cloudflare R2** |
| 偶爾分享私人檔案 | **pCloud / Dropbox / Google Drive** |

---

# 12. 核心原則

1. **個人使用、團隊使用、公開分享是三種不同需求**
2. **Storage ≠ Traffic**
3. **同步強 ≠ 適合大量公開下載**
4. **收藏強 ≠ 適合頻繁修改**
5. **GitHub 適合程式碼頻繁修改，不代表適合所有檔案**
6. **大量公開發布優先考慮 Releases / Object Storage / CDN**
7. **重要資料永遠不要只有一份**

---

## 官方來源

- pCloud: https://help.pcloud.com/
- Dropbox: https://help.dropbox.com/
- Google Drive: https://support.google.com/drive/
- MEGA: https://help.mega.io/
- MediaFire: https://www.mediafire.com/
- GitHub: https://docs.github.com/
- Cloudflare R2: https://developers.cloudflare.com/r2/

> 各服務方案與限制可能隨時間調整，實際 Pricing、Help Center、Dashboard 顯示值優先。
