# 雲端儲存與分享使用指南

> 更新日期：2026-10-05  
> 本文以「**個人使用**」與「**分享使用**」為核心，快速比較常見雲端服務。  
> 評分是依一般使用情境做的定位評估，不是官方評分。實際方案與流量限制仍以各家官網為準。

---

## 先看結論

| 服務 | 個人存放 | 自己存取 / 同步 | 公開分享 | 大容量收藏 | 最適合做什麼 |
|---|---:|---:|---:|---:|---|
| **Google Drive** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ | 日常文件、照片、跨裝置 |
| **pCloud** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 長期收藏、冷資料、雲端總倉庫 |
| **Dropbox** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | 工作同步、多裝置、團隊協作 |
| **MEGA Free** | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | ⭐⭐ | 中轉、大檔臨時分享 |
| **MediaFire Free** | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐ | 免費公開下載 |
| **GitHub Releases** | ⭐⭐ | — | ⭐⭐⭐⭐⭐ | ⭐ | 程式、工具、版本發布 |
| **Cloudflare R2** | ⭐⭐⭐ | — | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 網站、Client、Patch、大流量下載 |

---

## 1. 先分清楚：個人使用 vs 分享使用

### 個人使用

指的是自己上傳、下載、跨裝置、同步、長期保存、當作網路硬碟。

這類用途最重要的是：

- Storage 容量
- 桌面同步體驗
- 自己下載速度
- Online-only / Stream / Virtual Drive
- 長期價格
- 是否適合大量冷資料

### 分享使用

指的是產生公開連結、給朋友下載、在 Discord / 論壇 / 網站貼下載連結，或讓大量使用者下載 Client / Patch / 工具。

這類用途最重要的是：

- Shared Link Traffic
- Public bandwidth
- Egress
- 每日／每月流量限制
- 熱門檔案是否會被暫停
- 是否適合當下載站

---

## 2. 容量與流量到底差在哪？

把雲端想成一座倉庫：

| 名稱 | 白話解釋 |
|---|---|
| **Storage** | 倉庫能放多少東西 |
| **Upload** | 你搬多少資料進倉庫 |
| **Download** | 你自己從倉庫拿回多少資料 |
| **Shared Traffic** | 別人透過分享連結拿走多少資料 |
| **Egress** | 雲端把多少資料送到 Internet |
| **Operations** | 讀、寫、列出檔案等操作次數 |

例如只存一個 **10GB** 檔案：

- Storage：只占 10GB
- 自己下載 3 次：30GB 傳輸
- 分享給 1,000 人：大約 10TB 分享流量

> **有 10TB 雲端空間，不代表可以免費對外傳 10TB、100TB。**

---

## 3. Google Drive

### 個人使用：⭐⭐⭐⭐⭐

**優點**
- Google 生態完整
- 文件、試算表、簡報協作成熟
- 手機、網頁、Windows 都方便
- Drive for desktop 支援 Stream / Mirror
- 搜尋與文件預覽很好用

**缺點**
- 長期收藏數 TB 時，成本通常不漂亮
- 不是為大型公開下載站設計

**適合**
- 日常文件、PDF、相片
- 工作文件、學校資料
- 手機與電腦跨裝置

### 分享使用：⭐⭐

Google 個人 Drive 沒有提供簡單的「每月可公開分享 X TB」數字。

熱門公開檔案短時間被大量下載時，可能出現：

> Too many users have viewed or downloaded this file recently.

**建議：**適合自己用與少量分享；不適合大量公開下載大型 Client、Installer、ZIP。

官方：
- https://support.google.com/drive/answer/2423534
- https://support.google.com/a/users/answer/7338880

---

## 4. pCloud

### 個人使用：⭐⭐⭐⭐⭐

**優點**
- 很適合長期收藏與冷資料
- 有 Lifetime 方案
- pCloud Drive 可當虛擬磁碟
- 大量資料不必完整占用本機空間
- 適合歷史版本、素材、壓縮封存

**缺點**
- 虛擬磁碟不等於高速 SSD
- 大量小檔案直接執行體感不一定理想
- 重要資料仍不建議只留一份

**適合**
- 大型收藏庫
- 歷史 Client
- 壓縮檔、素材、長期封存

### 分享使用：⭐⭐⭐

pCloud 有明確 Shared Link Traffic。

| 方案 | Storage | Shared Link Traffic | Upload Traffic |
|---|---:|---:|---:|
| Basic | 最多 10GB | 50GB / 月 | 約為容量 2 倍 / 30 日 |
| Premium | 500GB | 1TB / 月 | 最高 1TB / 30 日 |
| Premium Plus | 2TB | 4TB / 月 | 最高 4TB / 30 日 |
| Ultra | 10TB | 20TB / 月 | 最高 4TB / 30 日 |

**建議：**適合私人總倉庫 + 偶爾分享；不適合當無限 CDN 或熱門大型下載站。

官方：
- https://help.pcloud.com/article/plan-details
- https://help.pcloud.com/article/shared-link-traffic

---

## 5. Dropbox

### 個人使用：⭐⭐⭐⭐⭐

**優點**
- 多電腦同步成熟
- Online-only / Available offline 好用
- 頻繁修改的工作檔同步體驗很好
- 團隊協作完整

**缺點**
- 長期大量收藏通常不是價格最漂亮的選擇
- 如果只是多年不動的冷資料，優勢不如同步工作明顯

**適合**
- 工作資料
- 多裝置同步
- 團隊專案
- 頻繁修改的資料夾

### 分享使用：⭐⭐⭐⭐

| 方案 | 分享頻寬 |
|---|---:|
| Basic | 20GB / 日 |
| Plus / Family / Professional / Essentials / Standard / Business | 1TB / 日 |
| Advanced / Business Plus / Enterprise | 4TB / 日 |

**建議：**比 Google Drive 更適合穩定分享工作檔；但大量玩家下載 Client / Patch 仍不是最佳用途。

官方：
- https://help.dropbox.com/share/banned-links
- https://help.dropbox.com/sync/make-files-online-only

---

## 6. MEGA Free

### 個人使用：⭐⭐⭐

**優點**
- 隱私與加密定位鮮明
- 大型檔案中轉常見
- 網頁與桌面工具完整

**缺點**
- Free Transfer quota 容易影響大型下載
- 免費容量不適合當永久大型收藏總庫

**適合**
- 中轉
- 接收資料
- 臨時大檔
- 私人分享

### 分享使用：⭐⭐

MEGA Free 的重點是 **Transfer quota**。下載與串流都會消耗 Transfer。

Free 不宜用「固定每 6 小時一定有 X GB」理解，因為可用額度可能是動態的。

**建議：**適合臨時分享，不適合持續大量公開下載。

官方：
- https://mega.io/pricing
- https://help.mega.io/

---

## 7. MediaFire Free

### 個人使用：⭐⭐

**優點**
- 簡單
- 傳統檔案分享模式
- 不需要複雜設定

**缺點**
- 免費容量小
- 不適合私人收藏總庫
- 桌面同步不是核心優勢

### 分享使用：⭐⭐⭐⭐

目前 Basic：
- 約 10GB Storage
- 單檔上限約 5GB
- Ad-supported downloads
- 官方標示 Unlimited bandwidth & downloads

**適合：**MOD、補丁、小工具、ZIP、免費公開下載。  
**不適合：**私人大型雲端倉庫、數 TB 收藏。

官方：
- https://www.mediafire.com/
- https://www.mediafire.com/upgrade/

---

## 8. GitHub Releases

### 個人使用：⭐⭐

GitHub 本質不是私人雲端硬碟。

Repository 適合：
- Source code
- Markdown
- YAML / JSON
- 網站原始碼

不適合：
- 大型 Client
- ISO
- 大型壓縮收藏

### 分享使用：⭐⭐⭐⭐⭐

GitHub Releases 很適合公開發布軟體。

目前官方限制：
- 每個 Release 最多 1,000 個 assets
- 每個 asset 小於 2 GiB
- Release 總大小沒有上限
- Bandwidth usage 沒有上限

**適合：**工具、編譯成品、小型 Installer、版本更新、軟體發布。

官方：
- https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases

---

## 9. Cloudflare R2

### 個人使用：⭐⭐⭐

R2 是 Object Storage，不是一般消費者同步硬碟。

沒有 Google Drive / Dropbox 那種同步體驗，但適合：
- 網站
- Object Storage
- 大型檔案發布
- 程式串接

### 分享使用：⭐⭐⭐⭐⭐

Cloudflare R2 最大特色：

> **Internet Egress 免費**

Standard Storage 目前大致為：
- Storage：US$0.015 / GB-month
- Class A：US$4.50 / 百萬次
- Class B：US$0.36 / 百萬次
- Internet Egress：Free

仍會計算 Storage、Operations，以及特定儲存類型的 retrieval。

**適合：**Client、Patch、網站大型檔案、圖片、CDN / 下載站後端。

官方：
- https://developers.cloudflare.com/r2/pricing/

---

## 10. 桌面使用：Dropbox vs Google Drive vs pCloud

| 服務 | 桌面模式 | 最適合 |
|---|---|---|
| Dropbox | Online-only / Available offline | 工作同步 |
| Google Drive | Stream / Mirror | 文件與跨裝置 |
| pCloud | Virtual Drive | 大容量收藏與按需存取 |

檔案已完整存在本機時，速度主要看 SSD / HDD。

檔案只在雲端時，體感會受網路、快取、檔案數量與服務架構影響。

不建議直接從雲端虛擬磁碟執行：
- 幾萬個小檔案的遊戲 Client
- 開發環境
- Database
- 高頻率 Random Access 工作

這類資料更適合：

> 雲端保存 → 需要工作時下載回 SSD

---

## 11. 最後怎麼選？

### 如果重點是「自己用」

| 需求 | 建議 |
|---|---|
| 日常文件與跨裝置 | **Google Drive** |
| 多台電腦同步工作 | **Dropbox** |
| 大容量長期收藏 | **pCloud** |
| 臨時中轉 | **MEGA** |

### 如果重點是「給別人下載」

| 需求 | 建議 |
|---|---|
| 小工具／程式版本 | **GitHub Releases** |
| 免費分享小檔 | **MediaFire** |
| Client／Patch／網站大型下載 | **Cloudflare R2** |
| 偶爾分享私人檔案 | **pCloud / Dropbox / Google Drive** |

---

## 12. 最重要的原則

1. **個人雲端 ≠ 公開下載站**
2. **Storage ≠ Traffic**
3. **分享流量 ≠ 自己下載**
4. **同步強，不代表適合大流量分享**
5. **容量大，不代表適合長期公開下載**
6. **大量公開發布應優先考慮 Releases / Object Storage / CDN**
7. **重要資料永遠不要只留一份**

---

## 官方來源

- pCloud: https://help.pcloud.com/
- Dropbox: https://help.dropbox.com/
- Google Drive: https://support.google.com/drive/
- MEGA: https://help.mega.io/
- MediaFire: https://www.mediafire.com/
- GitHub Releases: https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases
- Cloudflare R2: https://developers.cloudflare.com/r2/

> 各服務方案與流量限制可能隨時間調整，實際 Pricing、Help Center、Dashboard 顯示值優先。
