# 毅和企業島｜寶山廠 3D 導覽

獨立 HTML 網頁，以 WebGL 呈現寶山廠模型，支援拖曳旋轉、滾輪及雙指縮放、自動環繞、廠房與公司車輛特寫。提供產品、公司故事、工程、永續、Facebook 與聯絡導覽。

## 模型與車隊

- 主廠直接讀取業主提供的「寶山廠分解圖.skp」，保留可見面、群組與元件的累積變換及基本材質顏色；匯出 74,599 個三角面。原 SKP 檔未修改。
- 使用模型現有幾何，未把歷年模型視為現況測量；網頁不含原始材質貼圖、施工標註及不可見圖層。
- 車輛依毅和公開粉絲頁相片重建為簡化 3D 模型：白色駕駛室、深紅車頭下緣、白／淺藍攪拌桶、紅環帶與毅和側門識別。並非車廠精密 CAD。
- 品牌島嶼、道路、樹木與導覽館舍為展示配置，非實際廠區總平面。
- 車輛參考：https://www.facebook.com/photo.php?fbid=1440548958087467

## 操作

- 滑鼠拖曳／單指：水平旋轉與俯仰；滾輪／雙指：縮放。
- 「回到全島」、「看寶山廠」、「看公司車輛」：切換視角。
- 「暫停動畫」：停止車隊；「自動環繞」：自動旋轉鏡頭。
- 鍵盤聚焦 3D 畫面後，方向鍵旋轉，`+`／`-` 縮放，Home 回到全島。
- 遵循系統減少動態偏好。需支援 WebGL 與 DecompressionStream 的新版瀏覽器。

## 發布與檔案

- GitHub： https://github.com/masonlin1029-pixel/yiho-concrete-products
- GitHub Pages 使用 `main` 根目錄的 `index.html`，並設置 `.nojekyll`。
- 網頁內含壓縮幾何與全部程式，不需要 CDN、API 金鑰或外部模型下載；亦可離線開啟。
- `viewer-3d.js` / `scene-3d.html`：本地 3D 程式與介面來源。
- `build-3d.mjs`：整合既有導覽、模型及程式，輸出 `index.html` 和 `dist/index.html`。
- `export-skp.cs`：透過已安裝的 SketchUp C API 唯讀匯出模型。

## 官方連結

- 公司官網：https://yiho-concrete.com.tw/
- Facebook：https://www.facebook.com/profile.php?id=100063971286601

產品規格及供應條件以公司正式確認為準。

