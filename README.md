# TJDe-Net
TJDehaze Dataset & TJDe-Net model

## Environment Requirements
The model has been tested and is confirmed to work in the following environment:
- **Python**: 3.7  
- **PyTorch**: 1.10.2  
- **CUDA**: 11.3  

---

## Pretrained Model
The pretrained model is saved in the following directory:  
TJDe-Net/checkpoint/outdoor

---

## Test Dataset
The test dataset is located in:  
TJDe-Net/data/TJDehaze/test  

The dataset contains:  
- **GT**: Ground truth images (original images).  
- **hazy**: Hazy images generated using a monocular depth estimation method combined with the atmospheric imaging principle.  

The TJDehaze dataset (Subset, currently released as a watermarked version for demonstration only) is available via Baidu Netdisk:  
https://pan.baidu.com/s/15wVP0POcUUgIEbJRF9MoLA?pwd=sbim (extraction code: sbim).

---

## Directory Structure
```bash
TJDe-Net/
│
├── checkpoint/
│   └── outdoor/        # Pretrained model weights
│       └── TJDeNet.pth # Pretrained model file
│
├── data/
│   └── TJDehaze/
│       ├── test/       # Test dataset
│       │   ├── GT/     # Ground truth images
│       │   │   └── 1_0.85_0.25.jpg   # Example ground truth image
│       │   └── hazy/   # Hazy images
│       │       └── 1_0.85_0.25.jpg   # Example hazy image
│
├── result/             # Directory for saving test results
│
└── test.py             # Testing script
```

---

## Test Results
After running the model, the test results will be saved in the `result` directory.

---

## Usage
To test the model, use the following command:
```bash
python test.py --model TJDeNet --dataset TJDehaze --exp outdoor
