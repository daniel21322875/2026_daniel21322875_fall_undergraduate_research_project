# 1504《小熊有約：兩岸風雲再起》互動分析圖

本資料夾提供 1504 調查資料的兩種互動式二維降維圖。可切換題目、查看受訪者點位與答案，也可在右側圖例開關回答類別。

## 互動圖

### MCA 受訪者圖

- [開啟 MCA 互動圖](https://daniel21322875.github.io/2026_daniel21322875_fall_undergraduate_research_project/Dimension%20Reduction%20Graph/1504-%E5%B0%8F%E7%86%8A%E6%9C%89%E7%B4%84%EF%BC%9A%E5%85%A9%E5%B2%B8%E9%A2%A8%E9%9B%B2%E5%86%8D%E8%B5%B7/mca_interactive_respondents.html)
- 檔案：[mca_interactive_respondents.html](./mca_interactive_respondents.html)

MCA 以 683 位 Q1–Q27 完整作答者建立座標基準，並將 24 位缺答者投影到同一座標系。點選「補充投影」圖例可顯示或隱藏這 24 位受訪者。選擇 Q1 可在滑鼠提示中查看自填文字；「開放式問答」選項可查看最後一題的回答。Q28 不納入分析。

### Spectral embedding 圖

- [開啟 Spectral embedding 互動圖](https://daniel21322875.github.io/2026_daniel21322875_fall_undergraduate_research_project/Dimension%20Reduction%20Graph/1504-%E5%B0%8F%E7%86%8A%E6%9C%89%E7%B4%84%EF%BC%9A%E5%85%A9%E5%B2%B8%E9%A2%A8%E9%9B%B2%E5%86%8D%E8%B5%B7/spectral_embedding_interactive_respondents.html)
- 檔案：[spectral_embedding_interactive_respondents.html](./spectral_embedding_interactive_respondents.html)

此圖以 707 位受訪者建立 k 近鄰圖，並用圖拉普拉斯特徵向量呈現二維座標。缺答者直接納入圖中；兩位受訪者的距離只比較雙方都有回答的 Q1–Q27，並依共同作答題數校正，不把空白當作一種答案。圖中使用 **k = 15**、**λ₂ = 1.5995**（平均邊權重正規化），**z10 = 100/707（14.1%）**。SE1 軸上的虛線標示 z10 範圍，可用圖例或上方按鈕開關。

## 操作方式

1. 使用上方選單切換題目；最後一個選項「開放式問答」可查看最後一題文字回答。
2. 將滑鼠移到點上查看受訪者 ID、作答類別與座標；Q1 題目可查看自填內容。
3. 點擊右側圖例的回答類別可顯示或隱藏該類點。
4. MCA 圖可透過「補充投影」圖例切換 24 位缺答者；Spectral embedding 圖可透過「缺答者」圖例切換 24 位缺答者。
5. Spectral embedding 圖可用「顯示 z10 邊界／隱藏 z10 邊界」按鈕或 z10 邊界圖例切換虛線。

## 分析範圍

- MCA 與 Spectral embedding 使用 Q1–Q27；Q28 為訪談聯繫意願題，不納入降維。
- 最後一題是開放式文字，只用於互動圖中查看回答，不作為 MCA 或 Spectral embedding 的輸入變數。
- MCA 的 24 位缺答者是補充投影；Spectral embedding 的 24 位缺答者則直接作為圖節點參與建圖。兩張圖的座標尺度與意義不同，不宜直接比較座標數值。
