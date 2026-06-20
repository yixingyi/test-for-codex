# 鸢尾花分类项目

这是一个面向 Python 初学者的完整机器学习分类项目。项目使用 scikit-learn 自带的鸢尾花数据，不需要额外下载数据。

## 项目内容

- 理解并检查数据
- 可视化花瓣特征
- 划分训练集和测试集
- 使用标准化与逻辑回归训练模型
- 使用准确率、分类报告、混淆矩阵和交叉验证评估模型
- 预测新样本并保存模型

## 运行方法

1. 打开命令行并进入本目录。
2. 安装依赖：`python -m pip install -r requirements.txt`
3. 启动 Notebook：`python -m jupyter notebook`
4. 打开 `iris_classification.ipynb`，从上到下运行全部单元格。

运行完成后，训练好的模型会保存在 `models/iris_logistic_regression.joblib`。

## 主要结果

固定随机种子后，逻辑回归通常能在测试集上获得约 90% 以上的准确率。实际结果以 Notebook 运行输出为准。

## 项目限制

鸢尾花数据规模较小且非常整洁，适合学习完整流程，但不能代表真实业务中的复杂数据。
