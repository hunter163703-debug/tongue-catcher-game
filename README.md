# 不要浪費喲 體感舌頭運動遊戲 (Tongue Exercise Web Game)

> **Assistive Technology · 舌頭控制與口腔動作練習**

這是一款基於純前端技術與瀏覽器視訊鏡頭（MediaPipe Face Mesh + 嘴部顏色與特徵重心追蹤）開發的輔助科技體感網頁遊戲。旨在透過趣味的「小貓舔盤子清除醬汁」情境，引導使用者或個案進行主動且細膩的舌頭伸展、上下左右方向控制與口腔動作復健練習。

---

## 🌟 核心特色

1. **體感鏡頭辨識**：
   - 透過瀏覽器直接啟用前鏡頭，不需安裝任何 App。
   - 結合 Face Mesh 人臉關鍵點與嘴唇區域（ROI）即時動態追蹤。
   - 動態粉紅特徵重心演算法，靈敏捕捉舌頭上下左右伸展與位移。
2. **多模式輔助操控**：
   - 支援體感相機、螢幕虛擬方向盤（D-pad）與鍵盤方向鍵。
   - 具備防顫抖「死區（Deadzone）」調節與「靈敏度倍率」滑桿，方便不同個案自訂手感。
3. **關卡難度分級（大小不一污點練習）**：
   - **第一關**：5 個大小黑紅醬汁污點（基礎四向練習）。
   - **第二關**：10 個大小黑紅醬汁污點（擴展幅度練習）。
   - **第三關**：20 個大小黑紅醬汁污點（滿盤細膩控制與耐力練習）。
4. **即時語音與音效回饋**：
   - 內建 Web Audio API 合成音效，每次舔乾淨污點皆有成就感音效與過關慶祝。
5. **純前端安全架構**：
   - 所有視訊影像辨識全在本地端瀏覽器完成，絕不傳輸或儲存任何影像與隱私資料。

---

## 🚀 線上體驗

- **正式發布網址**：[https://tongue-exercise-tw.netlify.app/](https://tongue-exercise-tw.netlify.app/)
- **相容裝置**：iPad / iPhone（iOS Safari，需於 HTTPS 環境下開啟）、Android 平板/手機（Chrome）、Mac / Windows 電腦（Chrome, Edge, Safari）。

---

## 📁 專案檔案結構

```text
20260905生生有token/
├── index.html                 # 主程式網頁（包含遊戲、UI 與追蹤邏輯）
├── tongue-catcher.html        # 備用同步網頁
├── cattongue.png              # 小貓舌頭素材圖示
├── favicon.png / favicon.ico  # 網站圖示
├── apple-touch-icon.png       # iOS 主畫面圖示
├── ANTIGRAVITY.md             # 專案規則與技術架構說明
├── PROJECT_NOTES.md           # 開發日誌、收工記錄與心得
└── README.md                  # 專案說明文件
```

---

## 🛠️ 本地開發與測試

可以直接以靜態網頁伺服器開啟（需支援 HTTPS 以調用相機）：

```bash
# 使用 npx serve
npx serve -l 3000

# 或直接將檔案部署至 Netlify / Vercel / GitHub Pages
```

---

## 📄 授權條款

MIT License
