# 量化多因子模型构建与测试

## 项目概述
本项目是作为统计专业（金融统计方向）在多因子量化模型方面的实践项目
涵盖数据分析、可视化、机器学习方面的实践
实现了从**数据获取→因子构建→测试→加权**的全流程量化分析。聚焦电气设备行业股票，通过传统统计方法与机器学习技术结合，构建了具备稳定预测能力的多因子模型数据获取，清洗与预处理，因子构建，因子测试，因子加权
## 项目亮点
- 🚀 **流程覆盖**：完整实现因子研究全链条，包含4类技术指标因子+3类基本面因子
- 📊 **双重加权方案**：传统ICIR加权与机器学习加权（XGBoost+凸优化）
- 🔍 **深度因子测试**：通过ICIR分析、Alphalens测试、互信息评估三维度验证因子有效性
- ⚡ **工程优化**：采用Tushare API批量获取数据，实现自动化预处理流水线

## 文件结构
```
factor                                 
├─ data                                
│  ├─ data_fetch.ipynb                  # 电气设备行业数据获取（日线行情+基本面）
│  ├─ electrical_daily_2024.csv         #日线数据
│  ├─ electrical_daily_basic_2024.csv   #基本面数据 
│  ├─ factor_construct.ipynb            #技术指标/基本面因子计算与预处理
│  └─ factors.csv                       #因子数据
├─ factor_weight                       
│  ├─ icir.ipynb                        #基于ICIR的因子加权）
│  └─ mach_learn.ipynb                  # 机器学习加权（线性回归/XGBoost/凸优化）                        
├─ PRD.md                              
├─ README.md                           
└─ requiremensts.txt                   

```
## 安装依赖

`pip install -r requirements.txt`
