# Jetson Nano

Jetson Nano 是 NVIDIA 推出的一款小型、低功耗的人工智能 (AI) 计算机，适用于嵌入式系统和边缘计算应用。它提供了强大的 GPU 计算能力，使开发者能够运行深度学习、计算机视觉和机器人相关任务。

## 主要特点
- **GPU**: 128 核 Maxwell 架构 GPU
- **CPU**: 四核 ARM Cortex-A57 处理器
- **内存**: 4GB LPDDR4
- **存储**: microSD 卡
- **接口**: 4 x USB 3.0, HDMI, DisplayPort, M.2, GPIO, I2C, I2S, SPI, UART
- **电源选项**: 5V/4A (DC 供电) 或 5V/2A (micro-USB)
- **操作系统**: Ubuntu-based NVIDIA JetPack SDK

## 安装指南
### 1. 下载 JetPack
JetPack SDK 是 Jetson Nano 的官方软件支持包，其中包含 Ubuntu 系统、CUDA、cuDNN、TensorRT 和其他 AI 框架。

下载链接: [NVIDIA 官方网站](https://developer.nvidia.com/embedded/jetpack)

### 2. 烧录系统
1. 下载最新的 Jetson Nano 镜像文件。
2. 使用 balenaEtcher 或 Raspberry Pi Imager 将镜像写入 microSD 卡。
3. 将 microSD 卡插入 Jetson Nano 并启动。

### 3. 初始设置
1. 连接键盘、鼠标和 HDMI 显示器。
2. 插入电源并启动设备。
3. 按照系统引导进行基本配置。

## 基本使用
### 运行 TensorFlow 和 PyTorch
Jetson Nano 预装了 TensorRT，可以加速深度学习推理。
```bash
sudo apt update && sudo apt install -y python3-pip
pip3 install --pre --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v46 tensorflow
pip3 install torch torchvision
```

### 运行示例代码
```python
import torch
print("Is CUDA available:", torch.cuda.is_available())
```

## 资源链接
- [官方文档](https://developer.nvidia.com/embedded-computing)
- [Jetson Nano 开发者论坛](https://forums.developer.nvidia.com/c/jetson)
- [Jetson AI 课程](https://developer.nvidia.com/embedded/learn/jetson-ai-certification-programs)

