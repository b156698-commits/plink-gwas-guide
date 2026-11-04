# PLINK / GWAS QC Guide

一個給 PLINK / GWAS 初學者使用的教學網站，整理常見的 GWAS Quality Control 流程、PLINK 指令，以及基本的 GWAS 結果判讀。

## 專案內容

目前網站包含：

- Missingness QC
- MAF & HWE
- LD Pruning
- Relatedness / PI_HAT
- PCA
- Association Analysis
- Significance Thresholds
- Manhattan Plot
- QQ Plot
- 實際應用分享（預留擴充區域）

## 專案特色

本專案使用 `AGENTS.md` 定義網站的：

- 專案目的
- 網站結構
- 視覺風格
- 頁面固定格式
- 檔案命名規則
- AI 新增或修改內容時應遵守的規則

因此之後只要提供新的 PLINK / GWAS 主題，AI 就可以依照同一套規則新增頁面，而不需要重新設計整個網站。

## 網站結構

```text
plink-gwas-guide/
├── AGENTS.md
├── README.md
├── index.html
├── css/
│   └── style.css
└── pages/
    ├── missingness.html
    ├── maf-hwe.html
    ├── ld-pruning.html
    ├── relatedness.html
    ├── pca.html
    ├── association.html
    ├── gwas-results.html
    ├── manhattan-plot.html
    └── qq-plot.html
```

## 本機瀏覽

直接開啟 `index.html` 即可瀏覽網站。

## GitHub Pages

將整個專案上傳到 GitHub repository 後，可在 Repository 的：

**Settings → Pages → Deploy from a branch**

選擇主要 branch 與 `/ (root)` 作為發布來源。

## 延伸方式

例如未來要求：

> 依照 AGENTS.md 新增一頁 Relatedness / PI_HAT 教學。

AI 應能判斷頁面分類、檔名、固定教學結構、配色與導覽更新方式。

同樣地，如果要求新增 Manhattan Plot 或其他 GWAS 結果判讀內容，AI 應將其歸類到 GWAS Results，而不是 PLINK Commands。
