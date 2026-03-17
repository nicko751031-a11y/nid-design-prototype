# 川果設計 NID Design Lab - 官網 Prototype

## 網站概覽

川果設計（NID Design Lab）官方網站原型，採用極簡高端設計風格，支援桌機與手機自動切版（RWD 響應式設計）。

**線上預覽：** https://nicko751031-a11y.github.io/nid-design-prototype/

## 頁面結構

| 檔案 | 頁面 | 說明 |
|------|------|------|
| `index.html` | 首頁 | Hero 全螢幕視差背景、獎項列、作品集、服務、設計理念、聯絡 CTA |
| `about.html` | 關於川果 | 品牌介紹、設計理念卡片、核心競爭力 |
| `services.html` | 服務項目 | 四大服務（住宅/商業/建築/全屋訂製）、設計流程時間軸 |
| `portfolio.html` | 作品集 | 篩選分類、卡片式作品展示 |
| `project.html` | 作品詳情 | 圖片燈箱、專案資訊、上下篇導航 |
| `awards.html` | 國際獎項 | 統計數據、獎項徽章、得獎時間軸、精選案例 |
| `contact.html` | 聯絡我們 | 聯絡資訊、表單、Google Map |

## 響應式設計（RWD）

所有頁面支援三個斷點自動切版：

| 斷點 | 裝置 | 主要變化 |
|------|------|----------|
| `> 1024px` | 桌機 | 完整版面，多欄 Grid |
| `768px - 1024px` | 平板 | Grid 降為 2 欄，間距縮減 |
| `< 768px` | 手機 | 漢堡選單、單欄排版、縮減 padding |
| `< 480px` | 小螢幕手機 | 進一步縮減版面 |

### 手機版功能
- 漢堡選單（全螢幕覆蓋式選單）
- 語言切換按鈕（中/英切換）
- 觸控友善的按鈕尺寸
- 圖片自適應裁切

## 技術細節

- **純 HTML/CSS/JS**：無需建置工具，直接開啟即可
- **圖片**：全部 base64 內嵌，無外部圖片依賴
- **字型**：Google Fonts（Cormorant Garamond、Inter、Noto Sans TC、Noto Serif TC）
- **動畫**：CSS transition + IntersectionObserver 滾動觸發
- **多語言**：中英切換（CSS class 控制顯示/隱藏）

## 設計系統

```
色彩：
  --primary:   #2C2C2C  （深灰主色）
  --secondary: #8C8C8C  （次要灰）
  --bg:        #F5F3F0  （米白背景）
  --accent:    #B8A88A  （金棕強調色）
  --text:      #1A1A1A  （文字色）

字型：
  英文襯線：Cormorant Garamond（標題）
  英文無襯線：Inter（UI/標籤）
  中文襯線：Noto Serif TC（標題）
  中文無襯線：Noto Sans TC（內文）
```

## 部署方式

目前透過 GitHub Pages 部署：

```bash
# 修改後推送即自動更新
git add -A
git commit -m "更新內容"
git push
```

## 檔案大小

| 檔案 | 大小 |
|------|------|
| index.html | ~1.5 MB |
| portfolio.html | ~3.5 MB |
| services.html | ~675 KB |
| awards.html | ~285 KB |
| contact.html | ~228 KB |
| about.html | ~172 KB |
| project.html | ~115 KB |

> 檔案較大是因為圖片以 base64 內嵌。正式版建議改用外部圖片 + CDN 加速載入。
