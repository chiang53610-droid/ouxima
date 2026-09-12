# ouxima — OSHIMA 英文型錄資料庫

Google Drive「**英文目錄**」資料夾的內容，已整理成可在 GitHub 上直接瀏覽、搜尋的 Markdown 型錄庫。

- 來源：<https://drive.google.com/drive/folders/1Y61eDLV7TiKN-mhyArNbDiO45WRSIlQO>（擁有者 `AD@oshima.co`）
- 快照日期：**2026-09-12**
- 內容：8 個分類、3 個子分類、**11 份機台型錄**（另有 4 個目前為空的資料夾）

## 👉 [完整索引請看 catalog/INDEX.md](catalog/INDEX.md)

---

## 快速導覽

| 分類 | 內容 |
| --- | --- |
| [1. Inspection](catalog/01-inspection/) | EagleAi / EagleAi Plus 智能驗布機 |
| [3. Spreading](catalog/03-spreading/) | M190G 機械手臂上料 |
| [5. Ironing & Shaping](catalog/05-ironing-and-shaping/) | OP-565III 領子修剪翻領定型機 |
| [6. Heat Transfer](catalog/06-heat-transfer/) | （目前無可存取檔案） |
| [7. Fusing Press](catalog/07-fusing-press/) | （目前無可存取檔案） |
| [11. Needle, Weighing Detection](catalog/11-needle-weighing-detection/) | 檢針、秤重檢測 — 成衣 / 食品飲料 / 通用 |
| [12. Boiler](catalog/12-boiler/) | （目前無可存取檔案） |
| [13. Others](catalog/13-others/) | PDP-2000 投影比對、SLS-190 拉布貼標 |

## 依型號查找

CW-150・CW-220・CW-300 ｜ CWL-300 ｜ EagleAi・EagleAi Plus ｜ M190G ｜
OMW-600・OMW-800・OMW-1000 ｜ ON-688CD6S・ON-688CDD6S ｜ ON-CM ｜ ON-RFID ｜
OP-565III ｜ PDP-2000 ｜ SLS-190

→ 對照表在 [catalog/INDEX.md](catalog/INDEX.md#依型號快速查找)

---

## 每一頁的內容格式

每份型錄各自一個 Markdown 檔，結構固定：

1. **中繼資料表** — 分類、型號、原始檔名與大小、Drive 連結、型錄版本日期
2. **Overview** — 原文的產品說明與賣點（保留英文原文）
3. **Specifications** — 整理成表格的規格
4. **原始擷取文字（verbatim）** — PDF 的完整文字擷取結果，一字未刪

第 4 節的用意是**不遺漏任何資訊**：第 3 節的表格若有判讀疑義，都能回到 verbatim 區段對照。

## 資料正確性說明

- 型錄 PDF 多為多欄排版，文字擷取後**欄位對齊會遺失**。凡是需要推定欄位對應的數值，
  頁面上都以 `※` 標記並附上說明；無法可靠還原的對照表（例如 ON-688CD6S 的
  「檢測高度 ↔ 鐵球檢出能力」、OMW 系列的秤重段尺寸），一律**不猜測**，改為列出原始數值
  並提示以 Drive 上的 PDF 為準。
- 所有頁面都附上原始 PDF 的 Drive 連結，需要看圖片、排版或正式報價時請開啟原始檔。

## 為什麼沒有把 PDF 原始檔放進 repo

本 repo 只收錄文字內容，沒有鏡像 PDF 二進位檔，原因是建立這份快照的執行環境其網路政策
封鎖了 `drive.google.com`，無法把檔案實際抓下來（總計約 28 MB）。
文字版反而更適合在 GitHub 上做全文搜尋；需要原始 PDF 時，每一頁都有直達連結。

若日後要把 PDF 一併納入，在可連外的環境下把檔案下載到對應的 `catalog/<分類>/` 目錄，
再更新 [`catalog/manifest.json`](catalog/manifest.json) 即可。

## 如何更新

Drive 上的型錄有異動時，重新擷取對應的 PDF 文字並更新該頁面；
新增或刪除檔案時，同步更新 [`catalog/manifest.json`](catalog/manifest.json)、
[`catalog/INDEX.md`](catalog/INDEX.md) 與該分類的 `README.md`。

`manifest.json` 收錄了每個資料夾與檔案的 Drive ID、大小與修改時間，可作為比對差異的依據。
