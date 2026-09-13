# Spiking-GSCViT: Membrane-Potential-Aware Grouped Self-Attention for Hyperspectral Image Classification

Official implementation of **Spiking-GSCViT**, a lightweight spiking neural network (SNN) for hyperspectral image classification (HSIC). 
This work extends the ANN-based **GSC-ViT** into the spiking domain by computing attention from continuous membrane potentials rather 
than lossy binary spikes.

- Paper: [https://ieeexplore.ieee.org/document/11686273]
- Original GSC-ViT: [IEEE TGRS 2024](https://ieeexplore.ieee.org/document/10472541)
- Code repository: https://github.com/yaoqiong123/Spiking-GSCViT

## Citation

If you find this code useful, please cite our paper and the original GSC-ViT paper.

### Our paper




## Requirements

We recommend using a conda environment.

```bash
conda create -n spiking-gscvit python=3.7
conda activate spiking-gscvit
```

Install PyTorch 1.11.0 + CUDA 11.3:

```bash
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 \
  -f https://download.pytorch.org/whl/torch_stable.html
```

Install other dependencies:

```bash
pip install numpy scipy scikit-learn einops timm torchsummary thop
```

Main dependencies:

- Python 3.7+
- PyTorch 1.11
- torchsummary
- thop
- einops
- timm
- scikit-learn
- numpy / scipy

---

## Data Preparation

Place the hyperspectral datasets under `./datasets`.

The data loader `utils.dataset.load_mat_hsi` expects the dataset name and dataset directory. Please check `utils/dataset.py` for the exact `.mat` file names and keys.

Example:

```text
./datasets/
├── IndianPines/
├── Salinas/
├── Botswana/
└── WHU_Hi_LongKou/
```

Supported dataset names in the current code include:

```text
ip, sa, botswana, whulk, whuhh, whuhc, ksc, pu, hrl, flt, hus, MUUFL, Trento
```

Please modify `utils/dataset.py` if your local file organization is different.




