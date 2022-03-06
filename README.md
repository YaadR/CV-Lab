# Deep Rectangling for Image stitching: A Learning Baseline
<p align="center">Lang Nie<sup>1</sup>, Chunyu Lin<sup>1 *</sup>, Kang Liao<sup>1</sup>, Shuaicheng Liu<sup>2</sup>, Yao Zhao<sup>1</sup></p>
<p align="center"><sup>1</sup>Institute of Information Science, Beijing Jiaotong University</p>
<p align="center"><sup>2</sup>School of Information and Communication Engineering, University of Electronic Science and Technology of China</p>
<p align="center"><sup>{nielang, cylin, kang_liao, yzhao}@bjtu.edu.cn, liushuaicheng@uestc.edu.cn</sup></p>

<div align=center>
<img src="https://github.com/nie-lang/DeepRectangling/blob/main/rectangling.jpg"/>
</div>

## Dataset (DIR-D)
The details of the dataset can be found in our paper. 

We release our testing results with the proposed dataset together. One can download it in in [Google Drive]() or [Baidu Cloud](https://pan.baidu.com/s/1z_xVnpOEItZEyaCLnUGKfw)(Extraction code: 1234).

## Training
#### Step 1: Download the pretrained vgg19 model
Download [VGG-19](https://www.vlfeat.org/matconvnet/pretrained/#downloading-the-pre-trained-models). Search imagenet-vgg-verydeep-19 in this page and download imagenet-vgg-verydeep-19.mat. 

#### Step 2: Train the network
Modidy the 'Codes/constant.py' to set the 'TRAIN_FOLDER'/'ITERATIONS'/'GPU'. In our experiment, we set 'ITERATIONS' to 100,000.

```
python train.py
```

## Testing
#### Pretrained model for deep rectangling
Our pretrained rectangling model can be available at [Google Drive]() or [Baidu Cloud](https://pan.baidu.com/s/1Rc_UvnCs6O_e0gkBE3i6_Q)(Extraction code: 1234). And place the four files to 'Codes/checkpoints/Ptrained_model/' folder.
#### Testing with your own model
Modidy the 'Codes/constant.py'to set the 'TEST_FOLDER'/'GPU'. The path for the checkpoint file can be modified in 'Codes/inference.py'.

```
python inference.py
```


## Meta
NIE Lang -- nielang@bjtu.edu.cn
```
