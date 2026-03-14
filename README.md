[English](#english-version) | [中文版](#chinese-version)

---

<a name="english-version"></a>
# 🔪 PDF PicKiller (English)
A high-performance Python utility designed to detect and bulk remove images, complex gradients (Shadings), and nested watermark objects (Form XObjects) from PDF files.

### ✨ Key Features

* **Deep Inspection**: Identifies standard images, various PDF shading types (Axial, Radial, etc.), and nested Form objects.
* **Smart Preview**: Instantly preview specific PDF internal images using the system's default viewer via commands (e.g., `P IM1`).
* **"Form Cracker"**: Automatically digs into nested Form XObjects to find and extract hidden raster images.
* **Auto-Decryption**: Built-in standard PDF decryption engine; processes encrypted documents directly without pre-processing.
* **Visual Interface**: Built with `rich` and `colorama` for beautiful progress bars and colored terminal feedback.

### 🧪 Technical Logic

The tool maps and processes PDF resources using the following logic:

* **Shading Coordinate Mapping**: For radial or axial gradients, the tool extracts the $Coords$ array for parsing:
    $$\text{Coords} = [x_0, y_0, r_0, x_1, y_1, r_1]$$
* **Object Resolution**: Recursively dereferences "Indirect Objects" to accurately locate the `/Subtype` (whether `/Image` or `/Form`) regardless of nesting depth.

### 🛠️ Installation

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/PDF-PicKiller.git](https://github.com/YOUR_USERNAME/PDF-PicKiller.git)
    cd PDF-PicKiller
    ```

2.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

### 🚀 Usage

Run the program:
```bash
python your_script_name.py
```

---

<a name="chinese-version"></a>
# 🔪 PDF PicKiller (中文版)

这是一个高性能的 Python 工具，专门用于探测并批量化删除 PDF 文件中的图像、复杂的渐变背景（Shadings）以及嵌套的水印对象（Form XObjects）。

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
