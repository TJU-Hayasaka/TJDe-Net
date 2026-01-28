# Paper

[![DOI](https://img.shields.io/badge/DOI-10.1109%2FTASE.2025.3587466-blue)](https://doi.org/10.1109/TASE.2025.3587466)

**Towards Robust Overhead Power Transmission System Condition Monitoring: A Large-Scale Dataset and Novel Image Dehazing Approach**  
*IEEE Transactions on Automation Science and Engineering* (IEEE TASE), 2025  
DOI: https://doi.org/10.1109/TASE.2025.3587466

<details>
  <summary><b>Abstract</b></summary>

In hazy weather with high humidity, insulators in overhead transmission lines are prone to flashover. However, fog reduces the sensitivity of image detection, which is a commonly used method for condition monitoring of electrical equipment. Traditional image dehazing methods struggle to handle the complex backgrounds found in the scene and lack compatibility with downstream detection tasks. To overcome the image degradation, this study introduces Tongji Dehaze Network (TJDe-Net), a dehazing network engineered to enhance the visual clarity of images captured by unmanned aerial vehicles (UAVs) during power equipment inspections in hazy conditions. This network leverages a Swin-Transformer architecture with deep recursive feature integration and a cubic attention mechanism, therefore mitigating atmospheric degradation effects. Another major advancement presented in this work is the creation of the TJDehaze dataset, a comprehensive collection of paired images specifically designed for power transmission domain. This dataset comprises both real and synthetically generated hazy images, crafted to mimic a wide range of atmospheric densities and challenges. TJDe-Net’s performance is thoroughly evaluated across multiple datasets, including real-world dataset, TJDehaze synthetic dataset and the SFID-improved dataset. These evaluations proved TJDe-Net’s superior dehazing efficacy, which significantly bolsters subsequent image detection tasks. Experimental outcomes confirm TJDe-Net’s robustness and adaptability in real-world scenes, thereby enhancing the reliability and efficiency of UAV-based inspections and suggesting extensive potential for applications requiring enhanced visual perception in adverse weather conditions.

</details>

---

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
`TJDe-Net/checkpoint/outdoor`

---

## Test Dataset

The test dataset is located in:  
`TJDe-Net/data/TJDehaze/test`

The dataset contains:

- **GT**: Ground truth images (original images).  
- **hazy**: Hazy images generated using a monocular depth estimation method combined with the atmospheric imaging principle.  

The TJDehaze dataset is available via Baidu Netdisk:  
https://pan.baidu.com/s/1rnO7ptR7UoNFvid7Hmr88g?pwd=7hnq (extraction code: 7hnq)

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
```

---
## Citation (BibTeX)
```bash
@article{yuan2025towards,
  title={Towards Robust Overhead Power Transmission System Condition Monitoring: A Large-Scale Dataset and Novel Image Dehazing Approach},
  author={Yuan, Zhikang and Yang, Dongjun and Wei, Zixiang and Tang, Junqiu and Gu, Miaosong and Jin, Lijun and Liu, Xianhui and Zhang, Yinyao},
  journal={IEEE Transactions on Automation Science and Engineering},
  year={2025},
  publisher={IEEE},
  doi={10.1109/TASE.2025.3587466}
}
```

