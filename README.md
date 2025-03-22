# FDCT项目《面向粵港澳跨境聯邦學習的差分隱私噪聲優化技術研究》的產業化研发现状及战略规划分析

## 项目背景与目标

随着粤港澳大湾区数字化转型的不断推进，跨境数据流动与隐私保护已成为区域技术创新的核心课题。基于此背景，本项目《面向粤港澳跨境联邦学习的差分隐私噪声优化技术研究》计划在FDCT项目的基金支持下开展。通过构建高可用的跨境联邦学习平台，解决在大规模跨境数据传输与模型训练过程中，如何有效保障隐私安全、提升学习精度与效率的等关键问题。

项目的研究目标主要围绕三大核心方向展开：
1. **噪声分布与学习精度的关联模型建立**：为差分隐私噪声优化提供理论基础，确保隐私保护符合高标准要求。
2. **高性能的噪声分布优化和生成算法设计**：提升联邦学习的精度与训练效率，满足大模型训练的性能需求。
3. **技术标准化与产业化推进**：将研究成果封装为标准运行库，进而與產業化聯邦學習平臺的整合，有效推动技术的产业化应用。

## 产业化研发现状及战略规划分析

### 一、坚实理论基础

#### 研发现状
本项目在差分隐私和联邦学习领域取得了显著的理论成果，已发表三篇信息安全顶级期刊代表作，为后续技术研发提供了坚实的理论支持：

- [[TDSC 2023]](https://ieeexplore.ieee.org/document/10061543) **Cai Jianping**, Liu Ximeng, Li Jiayin, Kim-Kwang Raymond Choo. Differentially Private Non-Negative Consistent Release for Large-Scale Hierarchical Trees[J]. IEEE Transactions on Dependable and Secure Computing, 2024, 21(1): 388-402, DOI: 10.1109/TDSC.2023.3253520. (**CCF A 類, JCR Q1, TOP**)
- [[TDSC 2024](https://ieeexplore.ieee.org/document/10426793)] **Cai Jianping**, Liu Ximeng, Ye Qingqing+, Liu Yang, Wang Yuyang, A Federated Learning Framework Based on Differentially Private Continuous Data Release[J]. IEEE Transactions on Dependable and Secure Computing , 21(5): 4879-4894, DOI: 10.1109/TDSC.2024.3364060. (**CCF A 類, JCR Q1, TOP**)
- [[TIFS 2024](https://ieeexplore.ieee.org/document/10711967)] **Cai Jianping**, Ye Qingqing+, Haibo Hu, Liu Ximeng, and Yanggeng Fu, Boosting Accuracy of Differentially Private Continuous Data Release for Federated Learning[J]. IEEE Transactions on Information Forensics and Security, 19: 10287-10301, DOI: 10.1109/TIFS.2024.3477325. (**CCF A 類, JCR Q1, TOP**)


这些理论成果的核心贡献包括：
- **噪声分布的提出**：充分證明的定理 [Thm. 1 in TDSC 2023] 發現大量差分隱私研究的本質可歸結為對「噪聲分佈」的優化!
- **噪声分布的有效性**：“Equivalent Aggregation Theorem”[Thm. 1 in TDSC 2024]的提出證明聯邦學習上優化噪聲分佈的有效性； [TDSC 2024] 提出的FLDPCR框架驗證噪聲分佈優化的顯著性能提升。
- **AuBCR模型**：AuBCR模型 [TIFS 2024] 的提出進一步增强隱私聯邦學習精度，並形成一套行之有效的噪聲分佈優化範式。

#### 后续研发战略规划
- **突破现有模型**：计划在现有FLDPCR框架的基础上，继续突破模型的限制。当前已经在FLDPCR新模型研发上取得了[重要突破](https://github.com/imcjp/FLDPCR-kTCR)，并计划将此项成果投稿至信息安全顶级期刊TIFS上。
- **噪声分布与精度关联研究**：系统性研究噪声分布特征与联邦学习精度的关系，计划进行大量实验，但受计算资源限制，目前未能全面展开。
- **深入噪声分布优化技术**：从参数模型角度深入开展噪声分布优化研究，作为后续研究方向。

### 二、将科研成果封装为标准化的Python库

#### 研发现状
目前，已发布以下Python标准库：
- **dpcrpy**：集成了包括研究成果在内的多个DPCR模型。
- **opacus-dpcr**：基于Opacus框架的扩展，支持用户将DPCR模型集成到现有应用中。

这些标准库已发布至pypi.org，全球用户可以通过以下方式安装并应用：
```bash
pip install dpcrpy
pip install opacus_dpcr
```

#### 后续战略规划
1. **资金支持与团队扩展**：标准化Python库的发布需要考虑各项技术细节，确保其健壮性。每个版本必须经过充分测试，以适应不同的用户环境。为此，需要更多人员参与文档维护、版本管理以及全面测试。若获得资金支持，将引入更多人员参与标准库的设计、测试和维护，促进项目成果推广，提高影响力。
2. **发布标准与支撑软件**：制定标准化发布规范，设计相应的支撑性软件，帮助新参与者专注于内容设计，减少重复劳动，提高研发效率。

### 三、将科研成果与FATE框架结合

#### 研发现状
目前，已将FLDPCR框架与FATE平台深度整合，发布了[FLDPCR4FATE项目](https://github.com/imcjp/FLDPCR4FATE)。该项目提供了便捷的一键部署机制，方便联邦学习合作方应用，已在福州大学支持的服务器上展示了实际成果，访问地址：[https://fate.cityu.mo.cn](https://fate.cityu.mo.cn)。

#### 后续战略规划
1. **企业级技术整合挑战**：将进一步投入研发，解决技术整合的复杂性，推动成果正式融入FATE框架，计划与微众银行或清华大学AIR实验室开展合作。
2. **产业化技术整合**：尽管目前已进行了一定的技术整合，但还未达到产业化标准。后续将结合产业发展现状进行更加深入的研发，推动技术的实际应用。

### 四、跨境通信技术研发

#### 研发现状
跨境通信面临诸多挑战，尤其是在保证数据安全和提高数据传输效率方面。为此，开发了“云隧智联”子项目，通过安全隧道机制构建专用网络，保证数据传输安全，并在一定程度上提高传输效率。

该“云隧智联”子项目已投入实际使用，经过测试，在确保数据安全的同时，提升了数据传输效率5%-10%，对联邦学习中的模型传输至关重要。访问地址：[https://sec.cn.caijp.cn/](https://sec.cn.caijp.cn/)

#### 后续战略规划
由于当前跨境数据传输依赖云计算平台，且缺乏项目经费支持，现阶段只能选择低配云服务进行实验。若获得后续项目支持，将部署性能更强的云计算平台，支持大规模数据安全传输，实现跨境联邦学习的参数模型传递。

---

#### 总结
本项目的产业化研发战略规划围绕科研成果的标准化、平台化以及产业应用推进展开。通过持续的理论创新、标准库发布、FATE平台整合与跨境通信技术研发，项目将加速技术产业化，并为粤港澳大湾区跨境数据流动与智能化转型提供坚实的技术支持。
