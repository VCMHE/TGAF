# Enhancing Infrared-Visible Image Fusion via Text-Guided Adaptive Feature Integration
Code and dataset for ***Enhancing Infrared-Visible Image Fusion via Text-Guided Adaptive Feature Integration***


## Abstract

Image fusion techniques aim to integrate complementary information from multiple modalities, such as infrared and visible images, to generate enhanced images that preserve both texture details and salient targets. Traditional methods often overemphasize low-level visual features, neglecting high-level semantic information, which limits their performance in downstream applications. This paper proposes a text-guided adaptive fusion network that incorporates language-based textual descriptions during feature extraction to capture semantic information effectively. An Adaptive Attention Fusion module dynamically integrates critical features from both modalities, while a simplified ResFormer module enhances the network's ability to perceive local details and global structures. Extensive experiments demonstrate that our method outperforms state-of-the-art approaches in both subjective visual quality and objective metrics, achieving significant improvements in high-level vision tasks such as semantic segmentation and object detection (e.g., a 8% increase in mIoU for semantic segmentation on the MSRS dataset). Our findings underscore the potential of text-guided fusion networks in advancing image fusion technology. 


## 🌐 Usage

### ⚙ Network Architecture

Our TGAF is implemented in ``net/TGAF.py``.

### 🏊 Training
**1. Virtual Environment**
```
# create virtual environment
conda create -n TGAF python=3.8
conda activate TGAF
#Install pytorch
conda install pytorch==2.0.0 torchvision==0.15.0 pytorch-cuda=11.8 -c pytorch -c nvidia
```
**2. datasets**

 https://pan.baidu.com/s/1zJGKJlrh1y6GNBCxmQy5Mg?pwd=i82q 

**3. Pre-Processing**

Run 
```
python data_process.py
``` 
and the processed training dataset is in ``'./VLFDataset_h5/MSRS_train.h5'``.

**4. TGAF Training**

Run 
```
python train.py
``` 

### 🏄 Testing

**1. Pretrained models**

The pre-trained models can be found at ``'./ckpt_20.pth'``.

**2. Test datasets**

Run 
```
python data_process.py
``` 
and the processed test dataset is in ``'./VLFDataset_h5/MSRS_test.h5'``.

**3. Results in Our Paper**

Run
```
python test.py
``` 
