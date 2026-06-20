# 支持向量机乳腺肿瘤数据分类

这是一个面向 Python 初学者的支持向量机（SVM）完整教学项目。项目使用 scikit-learn 自带的 Wisconsin Diagnostic Breast Cancer 数据，不需要额外下载。

> 本项目仅用于机器学习教学，不能用于真实医疗诊断或治疗决策。

## 项目内容

- 检查缺失值、重复值和类别分布
- 建立多数类基准模型
- 比较缩放前后的 SVM
- 使用 Pipeline 避免数据泄漏
- 通过 5 折交叉验证搜索核函数、C 和 gamma
- 评估准确率、恶性精确率、恶性召回率、ROC-AUC 和混淆矩阵
- 使用置换重要性解释模型
- 预测单个样本并保存完整 Pipeline

## 运行方法

1. 打开命令行并进入本目录。
2. 安装依赖：`python -m pip install -r requirements.txt`
3. 启动 Notebook：`python -m jupyter notebook`
4. 打开 `svm_breast_cancer.ipynb`，从上到下运行全部单元格。

运行完成后，模型会保存到 `models/svm_breast_cancer_pipeline.joblib`。

## 已验证结果

在固定随机种子下，本地完整运行得到：

- 测试集准确率：97.37%
- 恶性精确率：100.00%
- 恶性召回率：92.86%
- 标准化后训练集交叉验证 ROC-AUC：0.995

结果用于说明机器学习流程，不代表临床性能。

## 项目结构

```text
svm-breast-cancer-project/
├── svm_breast_cancer.ipynb
├── svm_breast_cancer_report.html
├── README.md
├── requirements.txt
└── models/                    # 运行 Notebook 后生成
```

## 项目限制

这是规模较小的教学数据。模型结果不能替代外部验证、临床标准或专业人员判断。
