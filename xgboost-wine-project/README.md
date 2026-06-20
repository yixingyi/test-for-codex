# XGBoost 葡萄酒多分类项目

这是一个面向机器学习初学者的完整 XGBoost 多分类项目。项目使用 scikit-learn 自带的葡萄酒数据，根据 13 个化学特征预测 3 个葡萄酒类别。

## 项目内容

- 检查缺失值、重复值和类别分布
- 建立多数类基准模型
- 训练第一个 XGBoost 分类器
- 使用 5 折交叉验证评估稳定性
- 使用随机搜索调整树数量、学习率、深度和采样比例
- 评估准确率、宏平均 F1、ROC-AUC、Log Loss 和混淆矩阵
- 使用置换重要性解释模型
- 预测单个样本并保存原生 JSON 模型

## 运行方法

1. 打开命令行并进入本目录。
2. 安装依赖：`python -m pip install -r requirements.txt`
3. 启动 Notebook：`python -m jupyter notebook`
4. 打开 `xgboost_wine_classification.ipynb`，从上到下运行全部单元格。

运行完成后，模型和元数据会保存在 `models/` 目录。

## 已验证结果

在固定随机种子下，本地完整运行得到：

- 初始模型交叉验证宏平均 F1：97.89%
- 随机搜索最佳宏平均 F1：97.28%
- 测试集准确率与宏平均 F1：100.00%
- 测试集 Log Loss：0.030

初始模型在交叉验证中略优于本次随机搜索，因此最终选择初始模型。这说明调参不保证提升。测试集只有 36 条记录，100% 准确率不能直接代表生产性能。

## 项目结构

```text
xgboost-wine-project/
├── xgboost_wine_classification.ipynb
├── xgboost_wine_classification_report.html
├── README.md
├── requirements.txt
└── models/                              # 运行 Notebook 后生成
```

## 数据说明

数据集只有 178 条记录，适合教学和流程演示，不能代表大型生产数据集的复杂度。
