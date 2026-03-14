# 🔪 PDF PicKiller

这是一个高性能的 Python 工具，专门用于探测并精确删除 PDF 文件中的图像、复杂的渐变背景（Shadings）以及嵌套的水印对象（Form XObjects）。

## ✨ 核心功能

* **深度探测**：识别标准图像、各种 PDF 渐变类型（线性、径向等）以及嵌套在 Form 中的对象。
* **智能预览**：通过指令（如 `P IM1`）立即调用系统默认查看器预览指定的 PDF 内部图像。
* **“画框粉碎机”**：自动挖掘嵌套的 Form XObjects，寻找并提取隐藏的位图资源。
* **自动解密**：内置 PDF 标准解密引擎，无需预处理即可直接操作加密文档。
* **可视化界面**：基于 `rich` 和 `colorama` 构建，拥有美观的进度条和彩色终端反馈。

## 🧪 技术原理

该工具通过以下逻辑对 PDF 资源进行映射与处理：

* **渐变坐标映射**：对于径向或线性渐变，程序会提取其 $Coords$ 数组进行解析：
    $$\text{Coords} = [x_0, y_0, r_0, x_1, y_1, r_1]$$
* **对象解析**：递归地对“间接对象”（Indirect Objects）进行解引用，无论其嵌套多深，均能准确定位其 `/Subtype` 是 `/Image` 还是 `/Form`。

## 🛠️ 安装步骤

1.  **克隆仓库**
    ```bash
    git clone [https://github.com/你的用户名/PDF-PicKiller.git](https://github.com/你的用户名/PDF-PicKiller.git)
    cd PDF-PicKiller
    ```

2.  **安装依赖**
    ```bash
    pip install -r requirements.txt
    ```

## 🚀 使用指南

运行程序：
```bash
python your_script_name.py
