# CensNet
Code is from ["Co-embedding of Nodes and Edges with Graph Neural Networks"](https://arxiv.org/abs/2010.13242) (IEEE PAMI 2020) and ["CensNet: Convolution with Edge-Node Switching in Graph Neural Networks"](https://www.ijcai.org/Proceedings/2019/369) (IJCAI 2019)

# Prerequisites
* Python3
* Pytorch == 1.0.0 (with suitable CUDA and CuDNN version)
* Numpy
* argparse
* tqdm

# Dataset
The datasets (Cora, Citeseer and PubMed) are in [GoogleDrive](https://drive.google.com/file/d/1TXVTe2saZ80d26X5zhkqObhfhhTm6vyl/view?usp=sharing) and [BaiduPan (pw:frvg)](https://pan.baidu.com/s/1d5D5qApPvlYVdV5qWlUIgA).  
You need to move the dataset file into CensNet file.

# Training
You can run `python train.py` to train and evaluate.

The backbone of the model is CensNet. I added PairwiseDistance pretext task as self-supervised learning task.  Training stategy is joint learning, so the ssl pretext task is regarded as auxiliary task.