



[TOC]

# Anaconda 使用教程

### anaconda 常用命令

``````
activate // 切换到 base 环境

activate learn // 切换到 learn 环境

conda create -n learn python=3 // 创建一个名为 learn 的环境并指定 python 版本为 3 (的最新版本)

conda env list // 列出 conda 管理的所有环境

conda list // 列出当前环境的所有包

conda install requests 安装 requests 包

conda remove requests 卸载 requets 包

conda remove -n learn --all // 删除 learn 环境及下属所有包

conda update requests 更新 requests 包

conda env export > environment.yaml // 导出当前环境的包信息

conda env create -f environment.yaml // 用配置文件创建新的虚拟环境
``````

### anaconda 换源

换成清华的源

``````
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/

conda config --set show_channel_urls yes
``````

### 安装 pytorch

``````
conda install pytorch torchvision cudatoolkit=10.2 -c pytorch
``````

