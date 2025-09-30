# 舊主機轉址部署說明

這個 branch (redirect-legacy) 專門用於舊主機 (http://140.112.63.111/weiweng) 的 301 轉址設定。

## 部署步驟

1. 將此 branch 的檔案上傳到舊主機的 `/weiweng` 目錄
2. 確保 `.htaccess` 檔案生效（需要 Apache 支援）
3. 測試轉址是否正常運作

## 檔案說明

- `index-redirect.html`: 主要的轉址頁面（如果 .htaccess 不支援，可重新命名為 index.html）
- `redirect.html`: 備用的轉址頁面
- `.htaccess`: Apache 伺服器的 301 轉址設定
- `robots.txt`: 告訴搜尋引擎不要索引舊網站

## 轉址目標

所有流量將被導向新網站：https://slwstw.github.io/

## 注意事項

- 此 branch 不會 merge 回 main
- 舊主機的檔案部署後不再更新
- 新內容的更新請在 main branch 進行
- 建議保留舊主機轉址至少 6-12 個月，確保 SEO 完全轉移

## 測試轉址

部署後請測試以下 URL：
- http://140.112.63.111/weiweng/ (應轉址到 https://slwstw.github.io/)
- http://140.112.63.111/weiweng/about.html (應轉址到 https://slwstw.github.io/about.html)
- http://140.112.63.111/weiweng/news.html (應轉址到 https://slwstw.github.io/news.html)