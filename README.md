# CALENET: Enhanced Small Object Detection in Aerial Imagery through Context-Aware and Localization-Optimized Deep Learning

## Getting Started

### 1. Installation Requirements
CALENET is developed based on:
- **torch==2.0.0**
- **pytorch-cuda==11.8**

### 2. Clone Project
```bash
git clone https://github.com/lqh964165950/CALENET.git
cd CALENET
```

### 3. Create and Activate Conda Environment
```bash
conda create -n calenet -y python=3.9
conda activate calenet
```

### 4. Install PyTorch
```bash
conda install pytorch==2.0.0 torchvision==0.15.0 torchaudio==2.0.0 pytorch-cuda=11.8 -c pytorch -c nvidia
```

### 5. Install Dependencies
```bash
pip install -r requirements.txt
```

### 6. Prepare VisDrone Dataset
Make sure your dataset structure as follows:

```
VisDrone2019/
├── VisDrone2019-DET-train/
│   ├── images
│   └── labels
├── VisDrone2019-DET-val/
│   ├── images
│   └── labels
└── VisDrone2019-DET-test-dev/
    ├── images
    └── labels
```

### 7. Training CALENET
```bash
CUDA_VISIBLE_DEVICES=0 python train.py --weights '' --cfg /models/yolov5s-ELFN-PEM-DPFE.yaml --name 'CALENET'
```

---

