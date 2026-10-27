# 🎯 目標理財規劃器

以 PV（現值）、FV（終值）、PMT（每期存款）為核心的理財目標試算工具。純靜態網站（單一 `index.html`），無需建置。

## 功能
- 三種模式：求每月存款 PMT／求終值 FV／求現值 PV
- 目標範本（退休、購屋、教育、旅行、緊急預備金）
- 通膨調整、資產成長圖、保守／基準／樂觀情境比較
- 目標清單儲存於瀏覽器 localStorage

## 部署到 Cloudflare Pages（連結 GitHub）
1. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git
2. 選擇此 repository
3. Framework preset：None；Build command：留空；Build output directory：`/`
4. Save and Deploy

## 計算公式（每月複利，期末投入）
- i = 年報酬率 / 12，N = 年數 × 12
- FV = PV(1+i)^N + PMT × [((1+i)^N − 1) / i]
- PMT = (FV − PV(1+i)^N) × i / ((1+i)^N − 1)
- PV = (FV − PMT × [((1+i)^N − 1) / i]) / (1+i)^N

## 免責聲明
本工具僅供試算參考，不構成投資建議。

## License
MIT
