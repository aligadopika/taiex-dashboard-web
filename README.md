# 台股觀察儀表板（GitHub Pages）

這個資料夾可直接發布為 GitHub Pages 網站。網站讀取同目錄的 `data.json`，GitHub Actions 會在每個工作日台北時間 18:30 自動更新它。

## 發布步驟

1. 在 GitHub 建立一個新的公開儲存庫，例如 `taiex-dashboard`。
2. 將本資料夾內所有檔案上傳至儲存庫根目錄。
3. 在儲存庫 **Settings → Pages**，選擇 **Deploy from a branch**，Branch 選 `main`，資料夾選 `/(root)`，再儲存。
4. 等待部署完成後，GitHub 會顯示公開網址；可直接分享給朋友。
5. 如要立即更新，在 **Actions → Update dashboard data → Run workflow** 執行一次。

資料更新依賴 TWSE 與 Yahoo Finance 的公開資料端點；若來源暫時無回應，GitHub Actions 會顯示失敗，網站仍保留前一次成功快照。
