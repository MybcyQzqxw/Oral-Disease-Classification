# 口腔疾病分类系统

<div align="center">

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Next.js](https://img.shields.io/badge/Next.js-13-black.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-blue.svg)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC.svg)

**基于人工智能的口腔疾病图像分析系统**

[English](README.md) · **中文** · [在线演示](https://oral-disease-classification.vercel.app/) · [API文档](https://oraldiseasedetector.onrender.com)

</div>

## 📖 项目介绍

口腔疾病分类系统是一个先进的AI驱动应用程序，旨在通过图像分析识别各种口腔疾病。该工具利用最先进的深度学习和计算机视觉技术，为牙科诊断提供重要帮助。

### 🌐 部署链接
- **前端地址**: https://oral-disease-classification.vercel.app/
- **后端地址**: https://oraldiseasedetector.onrender.com
- **注意**: 训练接口仅在本地系统使用

## 📊 数据集介绍

### 牙科病症数据集
这是一个专门为牙科研究和分析精心策划的综合图像集合。该数据集涵盖了广泛的牙科病症，包括龋齿、牙垢、牙龈炎、牙齿变色、溃疡和牙齿缺失。它为牙科专业人士、研究人员和机器学习爱好者提供了宝贵的资源。

### 📋 数据集详情
- **图像类别**: 数据集包含精心标注的图像，分类为各种牙科病症：
  - **龋齿**: 显示蛀牙、空洞或龋齿病变的图像
  - **牙垢**: 描绘牙齿上牙垢或牙石堆积的图像
  - **牙龈炎**: 显示发炎或感染牙龈的图像
  - **牙齿变色**: 展示牙齿变色或染色的图像
  - **溃疡**: 显示口腔溃疡或口疮的图像
  - **牙齿缺失**: 表示缺失一颗或多颗牙齿状况的图像

### 🔗 数据集链接
[下载数据集](https://drive.google.com/file/d/13NFWEqtL_3Vxsr02ehXoYTapp63dMIDM/view?usp=drive_link)

## ✨ 主要特性

- **🖼️ 基于图像的疾病检测**: 用户可以上传口腔病症图像，系统将自动分类疾病
- **🧠 深度学习集成**: 集成先进模型以确保预测准确性
- **💻 交互式前端**: 易于使用的界面，提供即时反馈
- **🔄 DVC管道**: 轻量级实验跟踪和管道编排
- **📱 响应式设计**: 支持多设备访问

## 🛠️ 技术栈

### 前端
- **Next.js 13** - React框架
- **TypeScript** - 类型安全
- **TailwindCSS** - 样式框架

### 后端
- **Python** - 核心编程语言
- **Flask** - Web框架
- **DVC** - 数据版本控制
- **深度学习 & 计算机视觉** - AI模型
- **Transformers & HuggingFace** - 预训练模型
- **面向对象编程** - 代码架构

## 🚀 快速开始

### 环境要求
- Python 3.8+
- Node.js 16+
- Git

### 后端部署

1. **克隆仓库**
```bash
git clone https://github.com/Priyanshu9898/Oral-Disease-Classification.git
cd Oral-Disease-Classification
```

2. **创建Python虚拟环境**
```bash
python -m venv env
source env/bin/activate  # Linux/Mac
# 或
env\Scripts\activate     # Windows
```

3. **安装依赖**
```bash
pip install -r requirements.txt
```

4. **启动Flask后端**
```bash
python app.py
```

### 前端部署

1. **进入客户端目录**
```bash
cd client
```

2. **安装依赖**
```bash
npm install
```

3. **启动开发服务器**
```bash
npm run dev
```

4. **构建生产版本**
```bash
npm run build
```

## 📂 项目结构

```
Oral-Disease-Classification/
├── app.py                 # Flask应用主文件
├── main.py                # 主程序入口
├── requirements.txt       # Python依赖
├── params.yaml           # 参数配置
├── dvc.yaml              # DVC管道配置
├── config/               # 配置文件
├── src/                  # 源代码
├── client/               # 前端代码
├── research/             # 研究笔记本
├── Results/              # 训练结果
└── best_model/           # 最佳模型
```

## 🔄 工作流程

1. 更新 `config.yaml`
2. 更新 `secrets.yaml` [可选]
3. 更新 `params.yaml`
4. 更新实体
5. 在 `src/config` 中更新配置管理器
6. 更新组件
7. 更新管道
8. 更新 `main.py`
9. 更新 `dvc.yaml`
10. 更新 `app.py`

## 🎯 API接口文档

| 接口      | 方法   | 描述                           | 请求体示例                                                          | 成功响应示例                          | 错误响应示例             |
|-----------|--------|--------------------------------|-------------------------------------------------------------------|--------------------------------------|-------------------------|
| `/train`  | POST   | 触发模型训练                    | `{ "model_name": "模型名称" }`                                      | `{ "message": "模型训练完成" }`      | `{ "error": "错误信息" }` |
| `/predict`| POST   | 预测口腔疾病                    | `{ "image": "base64图像", "model_name": "可选模型名" }`             | `{ "prediction": "预测类别" }`       | `{ "error": "错误信息" }` |
| `/`       | GET    | Swagger文档链接                 | N/A                                                               | HTML内容                             | N/A                     |

### 📋 Swagger UI
- **地址**: `/swagger`
- 提供交互式API测试界面

## 📈 训练结果

| 模型              | 准确率     | 精确率     | 召回率     | F1分数     |
|:------------------|:-----------|:-----------|:-----------|:-----------|
| InceptionResnetV2 | 92.54%     | 91.06%     | 91.85%     | 91.32%     |
| efficientvit_m2   | 92.37%     | 91.74%     | 92.02%     | 91.74%     |
| efficientvit_m5   | 92.28%     | 92.15%     | 90.41%     | 90.80%     |
| EfficientNetB2    | 92.10%     | 92.39%     | 92.10%     | 92.21%     |
| efficientvit_b0   | 91.94%     | 90.54%     | 90.72%     | 90.61%     |
| EfficientNetB1    | 91.89%     | 91.84%     | 91.89%     | 91.73%     |
| DenseNet121       | 89.61%     | 89.71%     | 89.61%     | 89.57%     |
| MobileNetV2       | 89.44%     | 89.78%     | 89.44%     | 89.57%     |
| InceptionV3       | 84.29%     | 84.71%     | 84.29%     | 84.47%     |
| ResNet50          | 82.70%     | 82.80%     | 82.70%     | 82.19%     |

*完整结果请查看[Results目录](Results/)*

## 🗂️ DVC命令

```bash
# 初始化DVC
dvc init

# 重现管道
dvc repro

# 查看DAG
dvc dag
```

## 📊 数据准备

训练前需要准备数据集：

```bash
mkdir artifacts
cd artifacts
mkdir data_ingestion
cd data_ingestion
mkdir dataset
# 将6个数据类别文件夹解压到dataset目录中
```

## 🤝 贡献指南

欢迎贡献！请遵循以下步骤：

1. Fork 项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 🐛 问题反馈

如果您发现任何问题，请通过 [Issues](https://github.com/Priyanshu9898/Oral-Disease-Classification/issues) 页面报告。

## 📄 许可证

本项目基于 MIT 许可证开源 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 👨‍💻 作者

**Priyanshu Malaviya**

[![Portfolio](https://img.shields.io/badge/Portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://priyanshumalaviya.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/priyanshumalaviya/)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/Priyanshu2281)
[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@priyanshumalaviya9210)

## 🙏 致谢

- 感谢所有为开源社区贡献的开发者
- 特别感谢提供数据集的医疗机构
- 感谢 HuggingFace 和相关深度学习框架的支持

---

<div align="center">

**如果这个项目对您有帮助，请给个 ⭐️**

</div>
