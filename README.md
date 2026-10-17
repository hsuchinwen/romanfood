# 香榭食代有限公司（Roman Food CO., LTD.）官網

純靜態單頁網站（Tailwind CDN），不需要建置步驟。

## 檔案
- `index.html`：整個網站（首頁 + 商品詳細頁都在這一個檔案裡）
- `logo-mark.png`、`logo-full.png`：logo
- `images/`：商品照片

所有檔案與資料夾請放在同一層。

## 商品「第二頁」怎麼運作
- 首頁商品卡只顯示照片、名稱、售價，點擊卡片進入該商品詳細頁（網址會是 `index.html#p/a`、`#p/b`…）。
- 詳細頁的內容是從首頁商品卡自動讀取，所以**只要改首頁商品卡，詳細頁就會同步**，不用另外維護。
- 瀏覽器的「上一頁」可返回商品列表。

## 自己修改 index.html
1. 開啟網站，點右下角黑色鉛筆按鈕進入編輯模式。
2. 編輯模式下商品卡會展開全部欄位（口味、說明、包裝規格、售價），直接點文字修改；點照片可更換。編輯模式點商品卡不會跳頁。
3. 按上方「儲存並匯出 HTML」，下載新的 index.html 取代舊檔即可。
4. 新換的照片會直接內嵌在 index.html 內（檔案會變大），建議照片先壓縮到 1000px 以內，或把圖檔放進 `images/` 再改檔名。

## 上傳到 GitHub / Cloudflare Pages
把資料夾內所有檔案上傳到 Repository 根目錄。Cloudflare → Workers & Pages → 建立 → Pages → 連接 Git；Framework preset: None；Build command 留空；Build output directory: `/`。
