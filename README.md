### Getting started
CALENET: Enhanced Small Object Detection in Aerial Imagery through Context-Aware and Localization-Optimized Deep Learning

 **1. Installation** CALENET is developed based on torch==2.0.0 and pytorch-cuda==11.8.

 **2.Clone Project** 
git clone https://github.com/lqh964165950/CALENET.git

 **3.Create and activate a conda environment.** 
`conda create -n calenet -y python=3.9`
`conda activate calenet`
 **4. Install torch** 
`conda install pytorch==2.0.0 torchvision==0.15.0 torchaudio==2.0.0 pytorch-cuda=11.8 -c pytorch -c nvidia`
 **5. Install Dependencies** 
# Install required packages
pip install -r requirements.txt
6. Prepare VisDrone Dataset 
Make sure your dataset structure as follows:
├── coco
│ ├── annotations
│ │ ├── instances_train2017.json
│ │ └── instances_val2017.json
│ ├── images
│ │ ├── train2017
│ │ └── val2017
│ ├── labels
│ │ ├── train2017
│ │ ├── val2017
├── coco
│   ├── annotations
│   │   ├── instances_train2017.json
│   │   └── instances_val2017.json
│   ├── images
│   │   ├── train2017
│   │   └── val2017
│   ├── labels
│   │   ├── train2017
│   │   ├── val2017
7. Training CALENET
CUDA_VISIBLE_DEVICES=0 python train.py --weights '' --cfg /models/yolov5s-ELFN-PEM-DPFE.yaml  --name 'CALENET'