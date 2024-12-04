# Sudo Configurator

**Sudo Configurator** 是一個 macOS 專用的工具，用於快速為指定使用者設定 `sudo` 權限，並簡化相關操作。

[Release v1.0](https://github.com/ap311036/Sudo-Configurator/releases/download/v1.0/Sudo.Configurator.app.zip)

---

## 功能介紹

- **快速設定**：  
  為 macOS 使用者新增 `sudo` 權限，無需手動編輯 `/etc/sudoers` 文件。
  
- **安全驗證**：  
  使用 macOS 的系統授權機制進行操作，保證設定過程的安全性。

- **簡單易用**：  
  圖形化操作界面，適合對命令行不熟悉的使用者。

---

## 使用方法

1. **啟動應用**  
   打開 **Sudo Configurator**，應用會顯示對話框要求輸入相關資訊。

2. **輸入使用者名稱**  
   - 預設會自動填入當前登入的 macOS 使用者名稱。
   - 可自行修改為其他需要授予 `sudo` 權限的使用者名稱。

3. **確認操作**  
   - 點擊「繼續」以執行配置。
   - 系統將要求輸入管理員密碼進行驗證。

4. **完成操作**  
   - 成功配置後，可選擇開啟 `/etc/sudoers.d` 資料夾以檢查新增的設定文件。

---

## 開啟應用前的重要步驟

macOS 系統可能會將下載的應用標記為「受限」文件，導致無法執行。請依照以下步驟解除限制並正確啟動應用：

1. **移除 quarantine 標記**  
   在終端機中執行以下命令：  
   ```bash
   xattr -d com.apple.quarantine /path/to/SudoConfigurator.app
   
2. **設定執行權限**
   確保應用的主執行文件具備執行權限：
   ```bash
    chmod +x /path/to/SudoConfigurator.app/Contents/MacOS/*

3. **啟動應用**
點擊 SudoConfigurator.app 即可正常啟動。

## 注意事項

1. **系統權限**：  
   本應用需要管理員權限來修改 `/etc/sudoers.d` 資料夾的內容。

2. **正確格式**：  
   新增的 `sudo` 設定文件將遵循標準格式，例如：  
   `<username> ALL=(ALL) ALL`

4. **僅適用於 macOS**：  
本工具專為 macOS 系統設計，無法用於其他操作系統。

5. **謹慎使用**：  
為使用者新增 `sudo` 權限可能帶來安全風險，僅授予可信任的使用者。

---

## 錯誤處理

- 若出現「設定失敗」提示，請確認：  
- 提供的使用者名稱是否正確。
- 系統是否允許修改 `/etc/sudoers.d`。
- 輸入的管理員密碼是否正確。

- 若應用仍無法正常運作，請嘗試手動編輯 `/etc/sudoers.d` 文件或聯繫開發者。

---

## 開發者資訊

- **作者**：Sudo Configurator 團隊  
- **聯絡方式**：[admin@snoopyu.com](mailto:admin@snoopyu.com)
- **版本**：v1.0 
