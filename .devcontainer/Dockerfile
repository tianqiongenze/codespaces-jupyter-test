FROM nvidia/cuda:11.3.0-cudnn8-devel-ubuntu20.04

# 安装一些必要的依赖
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-dev \
    && rm -rf /var/lib/apt/lists/*

# 设置 Python 和 pip
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 1
RUN update-alternatives --install /usr/bin/pip pip /usr/bin/pip3 1

# 安装 PyTorch 和相关包
RUN pip install torch torchvision torchaudio

# 安装 JupyterLab
RUN pip install jupyterlab

# 设置工作目录
WORKDIR /workspace
