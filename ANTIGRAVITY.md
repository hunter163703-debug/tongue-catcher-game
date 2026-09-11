# ANTIGRAVITY.md - 專案規則與技術架構

## 專案概述
- **專案名稱**：不要浪費喲 體感舌頭運動遊戲
- **類型**：Web-based Assistive Technology Application
- **目標平台**：iPad Safari, Mobile Browsers, Desktop Chrome/Edge

## 技術架構與依賴
- **前端核心**：純 HTML5 + Vanilla JS + CSS3（Zero Build Dependency）
- **視訊辨識**：MediaPipe Face Mesh (CDN) + Custom ROI Tongue Color-Centroid Algorithm
- **圖形繪製**：HTML5 Canvas 2D API
- **音效系統**：Web Audio API Oscillator & Gain Nodes
- **部署平台**：Netlify (Site ID: `adb9d0de-5f95-494c-bc22-c54e945c4810`, URL: `https://tongue-exercise-tw.netlify.app`)
- **程式碼儲存庫**：GitHub (hunter163703-debug / tongue-exercise-tw)

## 開發與調校規範
1. **感應追蹤演算法**：
   - 嘴部 ROI 垂直邊界上方向鼻子延伸 `8%`，下方向下巴延伸 `12%`。
   - 嘴部 ROI 水平邊界左右各延伸 `8%`，確保個案向左右伸展舌頭時不被截斷。
   - 水平與垂直位移正規化採用臉部寬度/高度（`faceW * 0.20`, `faceH * 0.20`），增益係數維持對稱（`1.35x`）。
   - 平滑濾波係數設定為 `0.78 / 0.22`，兼顧跟手度與抗抖動。
2. **操控速度設定**：
   - 盤面基礎移動速度：水平 `420px/s`、垂直 `430px/s`。
   - 關卡配置：第 1 關 5 點、第 2 關 10 點、第 3 關 20 點（大小不一）。
3. **安全規範**：
   - 絕不將任何金鑰、個人或學生隱私資訊寫入程式碼或筆記。
