
<br />

#   This code has 2 versions:  



🦒 **Colab version (**Recommend**): inference and training mode! **Fast and easy to run****

👨‍💻 GitHub version: inference mode, but need to set up the environment.

##   📖 <a href="https://fmlinks.github.io/vessel-aneurysm-segmentation/docs/index.html" target="_parent\"><img src="https://img.shields.io/badge/Read-Document-blue" alt="Open In Colab"/></a>   🦒 <a href="https://colab.research.google.com/drive/1WS-u1ubEQaW7cGQ1R9IgW5Haytfduo1a?usp=sharing" target="_parent\"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>  🗂️ <a href="https://drive.google.com/drive/folders/10owYD1CuLUzUn_uQNt6koc7JMdeRBKQk?usp=sharing" target="_parent\"><img src="https://img.shields.io/badge/Download-Project-blue" alt="Open In Colab"/></a> 🕹️ <a href="https://drive.google.com/drive/folders/1tO_c9qi9-ckH_9krY_Fyihz4g5B5va8S?usp=drive_link" target="_parent\"><img src="https://img.shields.io/badge/Download-Dataset (requires authority)-blue" alt="Open In Colab"/></a> 








# VASeg: vessel-aneurysm-segmentation
Cerebrovascular and Aneurysm Segmentation in 3DRA images via a Deep Multi-Task Network


Weights can be download here: 

<a href="https://drive.google.com/file/d/1XZZY_H-Nt6mOZ3E9aFDAVvmYezxWJROi/view?usp=sharing" target="_parent\"><img src="https://img.shields.io/badge/Download-Weight-blue" /></a> fmnet5.hdf5 for inference_AneuristNet.py 

<a href="https://drive.google.com/file/d/1bIBnfGVuFZY_Ggye_vSUF41bdUfeR-tC/view?usp=sharing" target="_parent\"><img src="https://img.shields.io/badge/Download-Weight-blue" /></a> fmnet84.hdf5 for inference_Transformer.py 


Folder structure:

    vessel-aneurysm-segmentation/
    ├── data
    │   └── step0 (put the data you want to do inference here)
    │   │   └── ANSYS_UNIGE_09_image.nii.gz
    │   │   ├── ANSYS_UNIGE_28_image.nii.gz
    │   │   └── ...
    │   ├── step1 (pre-processed data, generate automatically)
    │   │   └── ANSYS_UNIGE_09_image.nii.gz
    │   │   ├── ANSYS_UNIGE_28_image.nii.gz
    │   │   └── ...
    ├── inference
    │   └── inference.ipynb (use this to do inference)
    │   ├── inference.py
    ├── results
    │   └── aneurysm (aneurysm prediction)
    │   │   └── ANSYS_UNIGE_09_image-[360, 633].nii.gz
    │   │   ├── ANSYS_UNIGE_28_image-[1540].nii.gz
    │   │   └── ...
    │   ├── vessel (vessel prediction)
    │   │   └── ANSYS_UNIGE_09_image_vessel_59969.nii.gz
    │   │   ├── ANSYS_UNIGE_28_image_vessel_68437.nii.gz
    │   │   └── ...
    ├── weights
    │   └── fmnet5.hdf5
    └── requirements.txt

How to use the code:

    cd vessel-aneurysm-segmentation
    pip install -r requirements.txt
    cd inference
    python inference_AneuristNet.py


Citation  ヾ(o′▽`o)ノ°°

    @article{lin2023high,
      title={High-throughput 3DRA segmentation of brain vasculature and aneurysms using deep learning},
      author={Lin, Fengming and Xia, Yan and Song, Shuang and Ravikumar, Nishant and Frangi, Alejandro F},
      journal={Computer Methods and Programs in Biomedicine},
      volume={230},
      pages={107355},
      year={2023},
      publisher={Elsevier}
    }
