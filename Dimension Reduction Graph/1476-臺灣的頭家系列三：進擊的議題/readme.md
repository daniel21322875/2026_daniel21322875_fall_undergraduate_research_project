# 1476《臺灣的頭家系列三：選舉的議題》互動分析圖

本資料夾提供 1476 調查資料的兩種互動式二維降維圖，可切換題目、查看受訪者點位與答案，也可點選圖例顯示或隱藏回答類別。

## 互動圖

### MCA 受訪者圖

- [開啟 MCA 互動圖](https://daniel21322875.github.io/2026_daniel21322875_fall_undergraduate_research_project/Dimension%20Reduction%20Graph/1476-%E8%87%BA%E7%81%A3%E7%9A%84%E9%A0%AD%E5%AE%B6%E7%B3%BB%E5%88%97%E4%B8%89%EF%BC%9A%E9%81%B8%E8%88%89%E7%9A%84%E8%AD%B0%E9%A1%8C/1476_mca_interactive_respondents.html)
- 檔案：[1476_mca_interactive_respondents.html](./1476_mca_interactive_respondents.html)

MCA 以 952 位在納入題目上完整作答的受訪者建立座標。分析排除前六個人口背景欄位、整份開放式問答，以及資料中全空白的 Q17 欄位；開放式問答只供互動圖檢視，不參與降維。本次納入 30 個類別變數，沒有缺答個案需要補充投影。

### Spectral Embedding 圖

- [開啟 Spectral Embedding 互動圖](https://daniel21322875.github.io/2026_daniel21322875_fall_undergraduate_research_project/Dimension%20Reduction%20Graph/1476-%E8%87%BA%E7%81%A3%E7%9A%84%E9%A0%AD%E5%AE%B6%E7%B3%BB%E5%88%97%E4%B8%89%EF%BC%9A%E9%81%B8%E8%88%89%E7%9A%84%E8%AD%B0%E9%A1%8C/1476_spectral_embedding_interactive_respondents.html)

此圖以相同的 30 個類別變數計算受訪者間的回答差異，建立 k 近鄰圖後取拉普拉斯特徵向量作為二維座標。設定為 **k = 15**、**λ₂ = 1.9270**（以平均邊權重正規化）、**z₁₀ = 50/952（5.25%）**；圖中標示一個連通分量。z₁₀ 邊界可由圖例或上方按鈕開關。

## 操作方式

1. 使用上方選單切換 Q1、Q2 等題目；題目文字會顯示在圖上方。
2. 將滑鼠移到點上，可查看資料列、回答類別與座標；有自填內容的選項也會顯示文字。
3. 點選右側圖例中的回答類別，可顯示或隱藏該類點。
4. 最後一個選單項目「開放式問答」只用來查看開放回答，不參與降維。
5. Spectral Embedding 圖可用「顯示 z₁₀ 邊界／隱藏 z₁₀ 邊界」按鈕或圖例切換邊界。

## 分析範圍與解讀

- 前六個人口背景欄位不納入降維；資料中全空白的 Q17 欄位也不納入。
- 最後一題開放式問答僅供查看回答，不作為 MCA 或 Spectral Embedding 的輸入變數。
- 目前納入的 952 位受訪者在 30 個分析欄位皆有作答，因此本次補充投影人數為 0。
- MCA 與 Spectral Embedding 的座標由不同方法計算，座標尺度和意義不同，不宜直接比較座標數值。

## 資料來源

資料來源為[微笑小熊調查小棧的調查資料庫](https://smilepoll.tw/web-s/survey_history.php)。本分析使用整理後的 1476 調查資料；問卷原始資料與報告請以資料提供平台及本專案所附文件為準。
