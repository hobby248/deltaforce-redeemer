# 三角洲兌換桌面助手（非官方）

Windows 桌面工具搭配 Chrome 擴充功能，批次輸入兌換碼並保存結果。

**本專案僅提供程式下載與使用說明，不公開 C# 原始碼。**

## 下載與安裝

1. [下載 Windows x64 v2.1.1](https://github.com/hobby248/deltaforce-redeemer/releases/download/v2.1.1/DeltaForceRedeemer-v2.1.1-win-x64.zip)。需要 Windows 11 x64；已內含 .NET，無需另行安裝。
2. 解壓縮整個 ZIP 到固定、可寫入的資料夾，開啟 `DeltaForceRedeemer.exe`。
3. [從 Chrome 商店安裝助手](https://chromewebstore.google.com/detail/edhpgaboajbmoljphpcdipibidpomiin)，不需開啟開發人員模式。
4. 開啟[官方兌換頁](https://redeem.df.garena.sg/zh-tw/cdkgarena.html)並手動登入，點助手「連線桌面工具」。
5. 在桌面貼上代碼，按「解析兌換碼」→「開始」。

只有安裝擴充功能無法批次兌換，桌面程式須同時開啟。已有舊手動版擴充功能時，請停用舊版避免同時連線。

## 功能

- 每行一組 Code，或 `Code-獎勵名稱`；只以第一個半形 `-` 分割，保留大小寫並去除重複。
- 每筆顯示結果、更新統計並保存 CSV／Log，正常結果後自動處理下一筆。
- 支援暫停、繼續、安全停止；關閉再開會恢復清單，不會自行開始。
- 「清除兌換紀錄」保留 Code 並重設待處理，原歷史先備份，方便自行切換網站帳號後再使用。
- CAPTCHA、登入失效、限流、斷線或結果逾時時暫停，交由使用者處理，不自動重送不明操作。

## 資料與更新

所有工具資料都在 EXE 所在資料夾：`Data` 保存清單，`Results` 保存歷史CSV及備份，`Logs` 保存日誌，`appsettings.json` 保存設定。Chrome 登入資料留在原 Chrome。

發布 ZIP 不含開發者的Code、Cookie、帳密或紀錄。更新時先關閉程式，備份並保留上述資料與設定；移動程式資料夾後重新開啟即可更新本機橋接登記。不要刪除 `NativeHost`。

若連線失敗，可執行「安裝與啟動.cmd」或主程式的「設定 Chrome 擴充功能」。包內 Extension 只作手動安裝備用。

## 版本與回報

- 桌面版本：v2.1.1
- 商店擴充功能：v2.0.3
- [最新下載](https://github.com/hobby248/deltaforce-redeemer/releases/latest)
- [問題回報](https://github.com/hobby248/deltaforce-redeemer/issues)：請附版本和錯誤文字，勿貼帳密、Cookie或其他私人資訊。

本工具非 Garena 官方產品，不提供兌換碼或繞過驗證，不保證所有代碼有效。遊戲名稱與圖示屬其權利人；本專案不宣稱官方合作關係。圖示取自[官方網站](https://web.df.garena.com/02_h5/240923_official_website/favicon.ico)。
