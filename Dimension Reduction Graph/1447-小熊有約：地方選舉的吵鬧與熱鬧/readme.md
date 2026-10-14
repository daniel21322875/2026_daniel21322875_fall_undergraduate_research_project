# 1447《小熊有約：地方選舉的吵鬧與熱鬧》互動分析圖

本資料夾提供 1447 調查資料的 PCA 與 Spectral Embedding 互動式二維圖。可切換題目、查看受訪者點位與回答，也可點擊圖例顯示或隱藏回答類別。

## 互動圖

### PCA 受訪者圖

- [開啟 PCA 互動圖](https://daniel21322875.github.io/2026_daniel21322875_fall_undergraduate_research_project/Dimension%20Reduction%20Graph/1447-%E5%B0%8F%E7%86%8A%E6%9C%89%E7%B4%84%EF%BC%9A%E5%9C%B0%E6%96%B9%E9%81%B8%E8%88%89%E7%9A%84%E5%90%B5%E9%AC%A7%E8%88%87%E7%86%B1%E9%AC%A7/1447_pca_interactive_respondents.html)
- 檔案：[1447_pca_interactive_respondents.html](./1447_pca_interactive_respondents.html)

以 718 位在分析題目上完整作答的受訪者建立 PCA 基準，另將 19 位缺答者投影到該座標系。Q4、Q5、Q19、Q21、Q41 不納入 PCA；缺答值以完整作答基準的題目平均補值，僅用於投影。PC1 解釋變異量為 **20.3%**，PC2 為 **11.5%**。

Q1–Q3、Q6–Q8 的 0–10 分數線性映射到 −1 至 1；其餘納入分析的 1–5 題映射為 −1、−0.5、0、0.5、1。「不確定」映射為 0。PCA 會中心化各題分數，不再逐題標準化。Q19、Q21 不參與 PCA，另計平均：映射分數平均分別為 **−0.135**、**0.353**；排除不確定回答後，原始 1–5 分平均分別為 **2.703**、**3.754**。

### Spectral Embedding 圖

- [開啟 Spectral Embedding 互動圖](https://daniel21322875.github.io/2026_daniel21322875_fall_undergraduate_research_project/Dimension%20Reduction%20Graph/1447-%E5%B0%8F%E7%86%8A%E6%9C%89%E7%B4%84%EF%BC%9A%E5%9C%B0%E6%96%B9%E9%81%B8%E8%88%89%E7%9A%84%E5%90%B5%E9%AC%A7%E8%88%87%E7%86%B1%E9%AC%A7/1447_spectral_embedding_interactive_respondents.html)
- 檔案：[1447_spectral_embedding_interactive_respondents.html](./1447_spectral_embedding_interactive_respondents.html)

Spectral Embedding 使用與 PCA 相同的分數映射及 36 個分析題目，以 718 位完整作答者建立 **k = 15** 的近鄰圖；19 位缺答者依已回答題目投影到同一座標系。圖中 **normalized λ₂ = 2.2366**、**z₁₀ = 218/718（30.36%）**，圖拉普拉斯有一個連通分量。z₁₀ 邊界可用上方按鈕或圖例切換。

## 操作方式

1. 使用上方選單切換 Q1–Q41，題目文字會顯示在圖上方。
2. 將滑鼠移到點上查看資料列、回答與座標；Q4 的小黨自填內容及 Q41 開放回答可在提示中查看。
3. 點擊右側圖例的回答類別，可顯示或隱藏該類點；隱藏類別不會改變座標縮放範圍。
4. PCA 圖中的補充投影以菱形標示；Spectral Embedding 圖也可切換補充投影點。
5. 最後一題 Q41 為開放式問答，只供查看回答，不參與降維。

## 分析範圍與解讀

- Q4、Q5、Q19、Q21、Q41 不納入降維基準；Q19、Q21 另行計算平均，Q41 只供查看開放回答。
- PCA 與 Spectral Embedding 使用不同的降維方式，座標方向與尺度不同，不宜直接比較座標值。
- PCA 軸上的百分比表示該主成分解釋的變異量；Spectral Embedding 的軸是圖拉普拉斯特徵向量座標，不代表原始題目的單一量尺。

## 資料來源

資料來源為[微笑小熊調查小棧的調查資料庫](https://smilepoll.tw/web-s/survey_history.php)。本分析使用整理後的 1447 調查資料；問卷原始資料與報告請以資料提供平台及本專案所附文件為準。

