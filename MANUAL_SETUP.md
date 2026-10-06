# 手動啟用 GitHub Pages 說明

## 背景

本倉庫包含「收據拍照，匯出報帳PDF」Android App 的隱私權政策頁面。所有必要的檔案（`index.html` 和 `README.md`）已經成功提交並推送到 `main` 分支。

## 需要手動完成的步驟

由於 API 權限限制，無法自動啟用 GitHub Pages。請按照以下步驟手動啟用：

### 步驟 1：登入 GitHub
使用具有此倉庫管理權限的 GitHub 帳號登入：https://github.com/login

### 步驟 2：前往 Pages 設定頁面
直接訪問：https://github.com/cvc016/receipt-privacy/settings/pages

或者：
1. 前往倉庫首頁：https://github.com/cvc016/receipt-privacy
2. 點擊頂部的「Settings」標籤
3. 在左側邊欄中，點擊「Pages」

### 步驟 3：配置 Pages 來源
在「Build and deployment」部分：
1. **Source**：選擇「GitHub Actions」（推薦，因為已配置自動部署 workflow）
   
   或者選擇「Deploy from a branch」：
   - **Branch**：選擇「main」
   - **Folder**：選擇「/ (root)」
   
2. 點擊「Save」按鈕

### 步驟 4：等待部署完成
- 如果選擇 GitHub Actions：workflow 會自動運行，通常需要 1-2 分鐘
- 如果選擇 Deploy from a branch：GitHub 會自動構建，通常需要 2-5 分鐘

頁面會顯示部署狀態和最終的 URL。

### 步驟 5：驗證網站
完成後，訪問：https://cvc016.github.io/receipt-privacy/

確認：
- ✅ 頁面返回 HTTP 200 狀態
- ✅ 頁面顯示「隱私權政策」標題
- ✅ 頁面包含聯絡郵箱：abbottabbott399@gmail.com
- ✅ 頁面包含應用名稱：「收據拍照，匯出報帳PDF」

## 已完成的工作

✅ 從上傳的檔案複製隱私政策為 `index.html`  
✅ 創建 `README.md` 說明本倉庫用途  
✅ 提交所有檔案到 `main` 分支  
✅ 推送到遠端倉庫  
✅ 配置 GitHub Actions workflow 用於自動部署（如果選擇 Actions 方式）  

## 技術細節

- **倉庫**：https://github.com/cvc016/receipt-privacy
- **分支**：main
- **最新提交**：4323b4d836adb1ac37972d4e421eb5313c30e99b
- **預期 URL**：https://cvc016.github.io/receipt-privacy/
- **應用套件名稱**：tw.receipt.expensepdf
- **聯絡郵箱**：abbottabbott399@gmail.com

## 自動部署（如果選擇 GitHub Actions）

倉庫已配置 `.github/workflows/static.yml`，啟用後：
- 每次推送到 `main` 分支時自動部署
- 使用 `actions/configure-pages@v4` 和 `actions/deploy-pages@v4`
- 完整的 CI/CD 流程無需手動介入

## 疑難排解

### 問題：Pages 設定頁面顯示 404
**原因**：您的帳號可能沒有倉庫的管理權限  
**解決**：聯繫倉庫擁有者 (cvc016) 授予您 Admin 或 Maintainer 權限

### 問題：workflow 運行失敗
**原因**：首次啟用 Pages 時，可能需要先手動啟用  
**解決**：按照上述步驟 3，先選擇「Deploy from a branch」啟用 Pages，之後再切換到「GitHub Actions」

### 問題：網站顯示 404
**原因**：部署尚未完成或配置錯誤  
**解決**：
1. 檢查 Actions 頁面：https://github.com/cvc016/receipt-privacy/actions
2. 確認最新的 workflow 運行成功（綠色勾號）
3. 等待 2-5 分鐘後重新訪問

---

如有任何問題，請聯繫：abbottabbott399@gmail.com
