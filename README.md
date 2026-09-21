# 銀行管理報表產生器

## 客戶使用方式

客戶不需要安裝 Python、PowerShell 或使用網頁。開啟交付資料夾，雙擊 `BankReportConverter.exe`，選擇 ERP Excel 與輸出資料夾後按下「產生管理報表」。

請將 `dist\BankReportConverter` 整個資料夾壓縮後交付，不能只複製 EXE。

## 建立交付版

開發者在已安裝 Python 3 的電腦上雙擊 `build_exe.bat`。批次檔會自動檢查並安裝 PyInstaller，然後使用 `bank_report_converter.spec` 建立 EXE。完成後交付 `dist\BankReportConverter`。

程式會產生管理報表、`validation_report.csv` 與 `unclassified_items.csv`。

## 客戶維護分類規則

主畫面點選「分類規則管理」即可新增、修改或刪除規則。可設定關鍵字、分類、優先順序、來源類別及完整備註比對，也可勾選「覆蓋範本原有分類」修改既有項目。分類欄可直接輸入新名稱。

客戶修改的規則保存在 `%APPDATA%\BankReportConverter\config`，更新或更換 EXE 時不會被覆蓋。新規則在下一次產生報表時立即生效。
# 網頁版（建議交付方式）

`docs/` 是可部署到 GitHub Pages 的純瀏覽器版本。客戶只要開啟網址、選擇 ERP 匯出的 `.xlsx`，即可下載管理報表，不需要安裝 Python、PowerShell 或 Windows EXE。

- Excel 在瀏覽器本機處理，不會上傳至伺服器。
- 分類規則可在畫面新增、刪除、匯入與匯出。
- 網站程式庫已放在 `docs/vendor/`，不依賴外部 CDN。
- GitHub Pages 設定方式請見 `docs/README.md`。
