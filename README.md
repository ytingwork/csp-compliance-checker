# CSP 合規性檢測工具 (CSP Compliance Checker)

![GitHub License](https://img.shields.io/badge/license-MIT-green)
![Category](https://img.shields.io/badge/Category-UI%20%2F%20Security-blue)

一個專為網頁前端、產品設計驗收（Design QA）與資安團隊打造的 **純前端、零依賴** CSP（Content Security Policy）合規性掃描工具。支援拖放 ZIP、專案資料夾或單段代碼，精準捕捉畫面層與代碼層的違規風險。

---

## 核心特點
*   **雙模式切換**：
    *   **介面驗收模式（預設）**：精準捕捉會破壞畫面渲染或阻擋 Transition 的「Inline JS 事件」與「Inline Style」。
    *   **資安稽核模式**：完整開啟 Unsafe-eval 核心邏輯與禁用開源套件（如老舊 Bootstrap / jQuery UI）之深度稽核。
*   **靈活配置匯入**：支援一鍵匯入自訂資安過濾規範（`.json`），與既有設計系統及安全政策高度同步。
*   **純本地安全運算**：所有檔案皆在瀏覽器沙盒內使用 FileReader 與 JSZip 批次解壓掃描，代碼不流向任何外部伺服器。
*   **優雅降級與無障礙設計**：內建防呆過濾，自動跳過圖片、影音及 `.min.js`，避免不必要的系統資耗。

---

## 實際介面與 UI 視覺
系統介面採用符合現代金融與高階工程工具有感之**深色調設計系統（Dark Mode First）**。視覺層級分明，提供高 scannability 的圖表資訊看板。

<img width="1980" height="995" alt="screencapture-file-Users-cfh01001792-Downloads-csp-compliance-checker-index-html-2026-07-15-11_59_02" src="https://github.com/user-attachments/assets/25a42df5-8a80-4d84-90bc-455413a99c5e" />

### 📊 主控制台與數據看板
*包含精準的總覽統計（Summary）與 Conic-gradient 圓餅圖，直觀呈現 Critical / High / Medium 的違規佔比。*

<img width="1980" height="3005" alt="screencapture-file-Users-cfh01001792-Downloads-csp-compliance-checker-index-html-2026-07-15-14_17_24" src="https://github.com/user-attachments/assets/c19ae8d7-d8da-480c-85c3-097cbc872174" />

### 🟢 檢測通過狀態 (All Clear)
*當所有掃描檔案皆符合資安與介面合規標準時，控制台將呈現全綠色的成功狀態指標，並附帶標準合規提示。*

<img width="2940" height="1914" alt="screencapture-file-Users-cfh01001792-Downloads-csp-checker-fixed-html-2026-07-14-11_38_29" src="https://github.com/user-attachments/assets/424a2de6-eb5d-4093-aa6a-d31ed0e708f9" />
