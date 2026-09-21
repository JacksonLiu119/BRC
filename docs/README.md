# 銀行明細管理報表轉換器（網頁版）

這是純前端靜態網站，可直接部署到 GitHub Pages。Excel 只在使用者瀏覽器內處理，不會上傳到伺服器。網站中的範本已移除客戶交易明細，只保留報表格式與必要分類設定。

## GitHub Pages

在 GitHub repository 的 **Settings → Pages**，將來源設為 **Deploy from a branch**，選擇 `main` 與 `/docs`。

客戶使用流程：開啟網址 → 選擇 ERP 匯出的 `.xlsx` → 按「產生並下載管理報表」。
