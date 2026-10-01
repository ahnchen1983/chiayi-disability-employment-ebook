# Google Sites 嵌入方式

這個資料夾是完整的電子繪本靜態網站，`index.html` 與 `pages/` 必須放在同一個網站根目錄。

## 建議方式：用網址嵌入

1. 將整個 `嘉義縣身障就業繪本電子書` 資料夾部署到可公開存取的靜態網站空間。
2. 取得 `index.html` 的公開網址。
3. 在 Google Sites 選擇「插入」→「嵌入」→「網址」。
4. 貼上網址後調整區塊高度；建議桌機至少 720 px，手機可設為 560 px 以上。

Google Sites 不支援把含有 JavaScript 的完整 HTML 直接貼到「嵌入程式碼」欄位，因此不能只貼一段 HTML 就完成翻頁功能。必須先把這個資料夾放到一個能提供 HTTPS 網址的靜態主機，再以網址嵌入。

## 若使用 iframe

將下列網址替換成實際部署網址後，可放在支援 HTML iframe 的頁面：

```html
<iframe
  src="https://你的網域.example/"
  title="我學會了看見不一樣｜嘉義縣電子繪本"
  style="width:100%;height:760px;border:0;border-radius:16px;"
  loading="lazy"
  allowfullscreen>
</iframe>
```

檔案內的圖片是由原始 PDF 頁面轉出的 JPG，沒有改寫繪本內容；翻頁動畫、鍵盤操作、全螢幕和觸控滑動由 `index.html` 提供。
