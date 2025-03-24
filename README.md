# FDCT項目《面向粵港澳跨境聯邦學習的差分隱私噪聲優化技術研究》的產業化研發現狀及戰略規劃

## A. 項目背景與目標

隨着粵港澳大灣區數字化轉型的不斷推進，跨境數據流動與隱私保護已成爲區域技術創新的核心課題。基於此背景，本項目《面向粵港澳跨境聯邦學習的差分隱私噪聲優化技術研究》計劃在FDCT項目的基金支持下開展。通過構建高可用的跨境聯邦學習平臺，解決在大規模跨境數據傳輸與模型訓練過程中，如何有效保障隱私安全、提升學習精度與效率的等關鍵問題。

項目的研究目標主要圍繞三大核心方向展開：
1. **噪聲分佈與學習精度的關聯模型建立**：爲差分隱私噪聲優化提供理論基礎，確保隱私保護符合高標準要求。
2. **高性能的噪聲分佈優化和生成算法設計**：提升聯邦學習的精度與訓練效率，滿足大模型訓練的性能需求。
3. **技術標準化與產業化推進**：將研究成果封裝爲標準運行庫，進而與產業化聯邦學習平臺的整合，有效推動技術的產業化應用。

## B. 產業化研發現狀及戰略規劃分析

### 一、堅實理論基礎

#### 研發現狀
本項目在差分隱私和聯邦學習領域取得了顯著的理論成果，已發表三篇信息安全頂級期刊代表作，爲後續技術研發提供了堅實的理論支持：

- [[TDSC 2023]](https://ieeexplore.ieee.org/document/10061543) **Cai Jianping**, Liu Ximeng, Li Jiayin, Kim-Kwang Raymond Choo. Differentially Private Non-Negative Consistent Release for Large-Scale Hierarchical Trees[J]. IEEE Transactions on Dependable and Secure Computing, 2024, 21(1): 388-402, DOI: 10.1109/TDSC.2023.3253520. (**CCF A 類, JCR Q1, TOP**)
- [[TDSC 2024](https://ieeexplore.ieee.org/document/10426793)] **Cai Jianping**, Liu Ximeng, Ye Qingqing+, Liu Yang, Wang Yuyang, A Federated Learning Framework Based on Differentially Private Continuous Data Release[J]. IEEE Transactions on Dependable and Secure Computing , 21(5): 4879-4894, DOI: 10.1109/TDSC.2024.3364060. (**CCF A 類, JCR Q1, TOP**)
- [[TIFS 2024](https://ieeexplore.ieee.org/document/10711967)] **Cai Jianping**, Ye Qingqing+, Haibo Hu, Liu Ximeng, and Yanggeng Fu, Boosting Accuracy of Differentially Private Continuous Data Release for Federated Learning[J]. IEEE Transactions on Information Forensics and Security, 19: 10287-10301, DOI: 10.1109/TIFS.2024.3477325. (**CCF A 類, JCR Q1, TOP**)

+項目顧問

這些理論成果的核心貢獻包括：
- **噪聲分佈的提出**：充分證明的定理 [Thm. 1 in TDSC 2023] 發現大量差分隱私研究的本質可歸結為對「噪聲分佈」的優化!
- **噪聲分佈的有效性**：“Equivalent Aggregation Theorem”[Thm. 1 in TDSC 2024]的提出證明聯邦學習上優化噪聲分佈的有效性； [TDSC 2024] 提出的FLDPCR框架驗證噪聲分佈優化的顯著性能提升。
- **AuBCR模型**：AuBCR模型 [TIFS 2024] 的提出進一步增強隱私聯邦學習精度，並形成一套行之有效的噪聲分佈優化範式。

#### 後續研發戰略規劃
- **突破現有模型**：計劃在現有FLDPCR框架的基礎上，繼續突破模型的限制。當前已經在FLDPCR新模型研發上取得了[重要突破](https://github.com/imcjp/FLDPCR-kTCR)，並計劃將此項成果投稿至信息安全頂級期刊TIFS上。
- **噪聲分佈與精度關聯研究**：系統性研究噪聲分佈特徵與聯邦學習精度的關係，計劃進行大量實驗，但受計算資源限制，目前未能全面展開。
- **深入噪聲分佈優化技術**：從參數模型角度深入開展噪聲分佈優化研究，作爲後續研究方向。

### 二、將科研成果封裝爲標準化的Python庫

#### 研發現狀
目前，已發佈以下Python標準庫：
- **dpcrpy**：集成了包括研究成果在內的多個DPCR模型。
- **opacus-dpcr**：基於Opacus框架的擴展，支持用戶將DPCR模型集成到現有應用中。

這些標準庫已發佈至pypi.org，全球用戶可以通過以下方式安裝並應用：
```bash
pip install dpcrpy
pip install opacus_dpcr
```

#### 後續戰略規劃
1. **資金支持與團隊擴展**：標準化Python庫的發佈需要考慮各項技術細節，確保其健壯性。每個版本必須經過充分測試，以適應不同的用戶環境。爲此，需要更多人員參與文檔維護、版本管理以及全面測試。若獲得資金支持，將引入更多人員參與標準庫的設計、測試和維護，促進項目成果推廣，提高影響力。
2. **發佈標準與支撐軟件**：制定標準化發佈規範，設計相應的支撐性軟件，幫助新參與者專注於內容設計，減少重複勞動，提高研發效率。

### 三、將科研成果與FATE框架結合

#### 研發現狀
目前，已將FLDPCR框架與FATE平臺深度整合，發佈了[FLDPCR4FATE項目](https://github.com/imcjp/FLDPCR4FATE)。該項目提供了便捷的一鍵部署機制，方便聯邦學習合作方應用，已在福州大學支持的服務器上展示了實際成果，訪問地址：[https://fate.cityu.mo.cn](https://fate.cityu.mo.cn)。網站頁面展示如下：

![image](https://github.com/imcjp/FDCT2025/blob/main/figs/fig_fate_web.jpg)

在上述網站上啟動算法後即可在後台看到運行結果，後台網站的訪問地址為 [https://fate.cityu.mo.cn](https://fateboard.cityu.mo.cn)。以下是後台內容展示：

![image](https://github.com/imcjp/FDCT2025/blob/main/figs/fig_fate_board.jpg)

#### 後續戰略規劃
1. **企業級技術整合挑戰**：將進一步投入研發，解決技術整合的複雜性，推動成果正式融入FATE框架，計劃與微衆銀行或清華大學AIR實驗室開展合作。
2. **產業化技術整合**：儘管目前已進行了一定的技術整合，但還未達到產業化標準。後續將結合產業發展現狀進行更加深入的研發，推動技術的實際應用。

### 四、跨境通信技術研發

#### 研發現狀

已初步成功研發了面向跨境通信項目“**雲隧智聯**”。該項目提供了高可靠的保證數據安全傳輸能力，同時提升數據傳輸效率。從而有效解決跨境通信面臨諸多挑戰。

其技術原理在於通過安全隧道機制構建專用網絡，從而提供可證明的數據傳輸安全保證；在隧道傳輸過程中引入數據壓縮機制，實現傳輸效率提升。

經過測試，“**雲隧智聯**”可在確保數據安全的同時提升了數據傳輸效率達5%-10%，有效滿足跨境聯邦學習對數據安全性和傳輸效率的需求。

目前，“**雲隧智聯**”已投入使用，用於支持前期的研發工作，並在和福州大學的合作中發揮關鍵作用。

以下是實際應用的展示：[https://sec.cn.caijp.cn/](https://sec.cn.caijp.cn/)。網站頁面展示如下（部分內容涉及隱私，故加馬賽克）：

![image](https://github.com/imcjp/FDCT2025/blob/main/figs/fig_sec_conn.jpg)

#### 後續戰略規劃
由於當前跨境數據傳輸依賴雲計算平臺，且缺乏項目經費支持，現階段只能選擇低配雲服務進行實驗。若獲得後續項目支持，將部署性能更強的雲計算平臺，支持大規模數據安全傳輸，實現跨境聯邦學習的參數模型傳遞。

## C. 總結
本項目的產業化研發戰略規劃圍繞科研成果的標準化、平臺化以及產業應用推進展開。通過持續的理論創新、標準庫發佈、FATE平臺整合與跨境通信技術研發，項目將加速技術產業化，併爲粵港澳大灣區跨境數據流動與智能化轉型提供堅實的技術支持。
