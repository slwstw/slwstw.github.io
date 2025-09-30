# 舊主機轉址部署說明

這個 branch (redirect-legacy) 專門用於舊主機 (http://140.112.63.111/weiweng) 的 301 轉址設定。

## 部署步驟

### 步驟 1: 上傳檔案
將此 branch 的所有檔案上傳到舊主機的 `/weiweng` 目錄

### 步驟 2: 測試 .htaccess
1. 先測試 `.htaccess` 是否生效
2. 訪問任何頁面（如 `about.html`）看是否自動轉址

### 步驟 3: 如果 .htaccess 不生效
如果分頁無法轉址，執行以下步驟：
1. 將 `index-redirect.html` 重新命名為 `index.html`
2. 將 `redirect-about.html` 重新命名為 `about.html`
3. 將 `redirect-news.html` 重新命名為 `news.html`
4. 將 `redirect-members.html` 重新命名為 `members.html`
5. 將 `redirect-publications.html` 重新命名為 `publications.html`
6. 將 `redirect-research.html` 重新命名為 `research.html`
7. 將 `redirect-teaching.html` 重新命名為 `teaching.html`

## 檔案說明

### 伺服器級別轉址
- `.htaccess`: Apache 伺服器的 301 轉址設定（優先選擇）
- `robots.txt`: 告訴搜尋引擎不要索引舊網站

### HTML 轉址檔案（.htaccess 備援方案）
- `index-redirect.html`: 首頁轉址（重新命名為 `index.html`）
- `redirect-about.html`: About 頁面轉址（重新命名為 `about.html`）
- `redirect-news.html`: News 頁面轉址（重新命名為 `news.html`）
- `redirect-members.html`: Members 頁面轉址（重新命名為 `members.html`）
- `redirect-publications.html`: Publications 頁面轉址（重新命名為 `publications.html`）
- `redirect-research.html`: Research 頁面轉址（重新命名為 `research.html`）
- `redirect-teaching.html`: Teaching 頁面轉址（重新命名為 `teaching.html`）

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