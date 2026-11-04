# AGENTS.md

## 1. 專案目的

本專案是一個「PLINK / GWAS 指令與 QC 知識網站」，主要提供 PLINK 1.9、GWAS Quality Control（QC）以及基礎 GWAS 結果判讀相關的教學內容。

網站希望將常見的 PLINK 指令與 GWAS 分析流程整理成容易查找與閱讀的網頁，協助初學者了解：

- 每個 QC 步驟的目的
- 常用 PLINK 指令
- 參數代表的意義
- 指令範例
- 執行時需要注意的事項
- 不同 QC 步驟之間的關係
- Association analysis 後常見的 GWAS 結果判讀方式

網站未來會持續增加新的 PLINK / GWAS 主題，因此 AI 新增或修改內容時，必須遵守本文件的結構與規則。

## 2. 目標使用者

主要使用者為：

- 剛開始接觸 PLINK 的學生
- 進行 GWAS 分析的初學者
- 希望快速查詢 PLINK 指令與 QC 流程的人

內容應以「容易理解，但保持技術正確」為原則。

## 3. 網站內容架構

網站內容依照 GWAS 分析流程分為四個主要部分。

### PLINK Basics
介紹：
- `.bed`
- `.bim`
- `.fam`
- `--bfile`
- `--make-bed`

### Quality Control
主要包含：
- Missingness
- MAF & HWE
- LD Pruning
- Relatedness
- PCA

### GWAS Analysis
主要包含：
- Phenotype
- Covariates
- Case-Control GWAS
- Logistic Regression
- `--logistic`

### GWAS Results
作為完成 association analysis 後的補充內容，包括：
- Suggestive significance
- Genome-wide significance
- Manhattan plot
- QQ plot

此部分主要是 GWAS 結果判讀，不應誤寫成 PLINK QC 指令。

## 4. 專案資料夾結構

目前專案使用以下結構：

```text
plink-gwas-guide/
│
├── AGENTS.md
├── README.md
├── index.html
│
├── pages/
│   ├── missingness.html
│   ├── maf-hwe.html
│   ├── ld-pruning.html
│   ├── relatedness.html
│   ├── pca.html
│   ├── association.html
│   ├── gwas-results.html
│   ├── manhattan-plot.html
│   └── qq-plot.html
│
└── css/
    └── style.css
```

規則：
- `index.html` 為首頁。
- 所有教學頁面放置於 `pages/`。
- 所有頁面共用 `css/style.css`。
- 不應在每個 HTML 中重複撰寫大量 CSS。
- 若未來加入圖片或圖檔，可建立 `assets/images/` 統一放置。

## 5. 首頁固定結構

首頁依照以下順序：

1. Hero
2. GWAS Workflow
3. Quality Control
4. GWAS Analysis
5. GWAS Results
6. 實際應用分享
7. Beginner Guide 與 Important Note
8. Footer

首頁中的 GWAS Results 必須清楚標示為結果判讀，不可誤寫為 PLINK Commands。

## 6. 一般教學頁固定結構

新增 PLINK / QC 教學頁面時，原則上依照以下結構：

1. 主題名稱
2. 這一步在做什麼？
3. 使用時機
4. PLINK 指令
5. 參數說明
6. 指令範例
7. 注意事項
8. 上一頁 / 回到首頁 / 下一頁

## 7. GWAS 結果補充頁規則

網站內容不限於 PLINK 指令。

若某個概念是理解完整 GWAS 分析流程的重要內容，例如：

- Suggestive significance
- Genome-wide significance
- Manhattan plot
- QQ plot

可以新增補充教學內容，但 AI 必須清楚區分「PLINK 操作」與「GWAS 統計結果判讀」。

## 8. PLINK 指令撰寫規則

PLINK 指令、參數與檔案格式保留英文，例如：

- `--geno`
- `--mind`
- `--maf`
- `--hwe`
- `--indep-pairwise`
- `--pca`
- `--logistic`
- `.bed`
- `.bim`
- `.fam`

指令必須使用程式碼格式呈現。

## 9. QC Threshold 規則

網站中的 threshold 若只是示範，必須清楚標示為「範例」。

不要描述成所有 GWAS 分析都必須採用的固定標準。

實際 threshold 應依：
- 資料品質
- 研究設計
- 樣本特性
- 分析目的

進行調整。

## 10. 網頁視覺風格

網站整體採用「柔和生物資訊教學風」。

主要使用：
- 奶油白背景
- 淡藍色
- 淡綠色
- 白色
- 少量淡黃色或淡橘色

可使用：
- DNA
- chromosome
- SNP
- genotype matrix
- 資料分析圖示

避免：
- 大面積純黑背景
- 高飽和霓虹色
- 強烈科技藍光
- 過多漸層或發光效果

主題卡片使用圓角、柔和背景色、輕微陰影或邊框與足夠留白。

## 11. 檔案命名規則

HTML 檔案名稱必須：
- 使用英文
- 全部小寫
- 使用 kebab-case
- 不使用空格
- 不使用中文檔名

例如：
- `missingness.html`
- `maf-hwe.html`
- `ld-pruning.html`
- `relatedness.html`
- `association.html`
- `gwas-results.html`

## 12. AI 新增頁面的流程

當使用者要求新增 PLINK / GWAS 主題時，AI 應：

1. 先閱讀 `AGENTS.md`
2. 判斷內容分類
3. 決定符合規則的檔名
4. 在 `pages/` 建立新的 HTML
5. 參考現有頁面版型
6. 使用固定教學結構
7. 使用既有 `css/style.css`
8. 更新首頁的相關入口
9. 必要時更新上一頁與下一頁導覽
10. 確認所有相對路徑正常
11. 不任意改變網站整體視覺風格

## 13. AI 修改既有內容時的規則

修改頁面時：
- 優先保留既有網站結構與設計
- 不要因新增一個主題重新設計整個網站
- 不刪除其他正常運作的頁面
- 不隨意更改既有檔名
- 新增內容應遵守固定格式
- 修改後確認導覽連結正常

## 14. 專案延伸原則

例如使用者要求：

> 依照 AGENTS.md 新增一頁 Relatedness / PI_HAT 教學。

AI 應能自行判斷：
- 此內容屬於 Quality Control
- 檔名應為 `relatedness.html`
- 頁面應放置於 `pages/`
- 使用既有教學版型
- 延續奶油白、淡藍、淡綠的視覺風格
- 更新首頁入口
- 更新必要的頁面導覽

如果使用者要求新增 Manhattan Plot 教學，AI 應將其歸類於 GWAS Results，而不是 PLINK Commands。

本專案最重要的原則是：

> 即使之後新增不同的 PLINK 或 GWAS 主題，AI 仍可以依照同一套專案規則持續擴充網站，而不需要重新設計整個網站。
