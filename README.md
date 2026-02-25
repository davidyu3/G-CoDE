# G-CoDE

***
**Graph-Correspondence Distillation for Gene Expression Prediction via Privileged Spatial Transcriptomics.**

Yichen Dai, Yuanyuan Chen, Yong Xia*
***

*Summary*: We propose G-CoDE, a novel privileged learning framework for robust image-to-gene expression prediction. G-CoDE introduces a differentiable graph matching regularizer to enforce cross-modal topological consistency between H&E images and privileged ST data, and a structure-preserving distillation module to transfer both feature-level and topological-level knowledge to a deployable image-only student model. Extensive experiments on three public ST datasets demonstrate that G-CoDE achieves SOTA performance, with significant improvements in both prediction accuracy and biological plausibility. Our method unlocks the potential for low-cost, high-throughput spatial transcriptomic profiling from routine H&E slides, with broad applications in computational pathology and biomedical research

<img src="./imgs/Framework.png" title="G-CoDE"/>


## Requirements
- Python 3.10.16
- Install the required packages by:
```bash
  pip install -r requirements.txt
```

## Data Preparation
### Step 1: Download Data
· STNet and Skin Dataset can be downloaded [here](https://drive.google.com/drive/folders/13oJqeoU5_QPy4_yeZ4eK694AGoBuQjop?usp=drive_link).\
· PCW and Mouse Dataset from STimage-1K4M can be downloaded according to [STimage-1K4M](https://github.com/JiawenChenn/STimage-1K4M).\
· INT and ZEN (including ZEN40-ZEN49) datasets from HEST-1k can be downloaded according to [HEST-1k](https://github.com/mahmoodlab/hest).
Save these datasets to ./data within your project workspace, the structure of ./data is:
```
    ├── dataset
    │   ├── Her2st
    │   ├── CSCC_data
    │   ├── Alec_NatGen
    │   │   ├── PCW
    │   │   └── Mouse
    │   └──HEST-1k
    │       └──ST
    │           ├── INT
    │           └── ZEN
    ├── data
    │   ├── filtered_expression_matrices
    │   ├── preprocessed_expression_matrices
    │   ├── skin
    ├── her2st_pred_att
```


