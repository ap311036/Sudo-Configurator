# Sudo-Configurator
Sudo Configurator 是一個 macOS 專用的工具，用於快速為指定使用者設定 sudo 權限，並簡化相關操作。

功能介紹
快速設定：
為 macOS 使用者新增 sudo 權限，無需手動編輯 /etc/sudoers 文件。

安全驗證：
使用 macOS 的系統授權機制進行操作，保證設定過程的安全性。

簡單易用：
圖形化操作界面，適合對命令行不熟悉的使用者。

使用方法
啟動應用
打開 Sudo Configurator，應用會顯示對話框要求輸入相關資訊。

輸入使用者名稱

預設會自動填入當前登入的 macOS 使用者名稱。
可自行修改為其他需要授予 sudo 權限的使用者名稱。
確認操作

點擊「繼續」以執行配置。
系統將要求輸入管理員密碼進行驗證。
完成操作

成功配置後，可選擇開啟 /etc/sudoers.d 資料夾以檢查新增的設定文件。
注意事項
系統權限：
本應用需要管理員權限來修改 /etc/sudoers.d 資料夾的內容。

正確格式：
新增的 sudo 設定文件將遵循標準格式，例如：

css
複製程式碼
<username> ALL=(ALL) ALL
僅適用於 macOS：
本工具專為 macOS 系統設計，無法用於其他操作系統。

謹慎使用：
為使用者新增 sudo 權限可能帶來安全風險，僅授予可信任的使用者。

錯誤處理
若出現「設定失敗」提示，請確認：

提供的使用者名稱是否正確。
系統是否允許修改 /etc/sudoers.d。
輸入的管理員密碼是否正確。
若應用仍無法正常運作，請嘗試手動編輯 /etc/sudoers.d 文件或聯繫開發者。

