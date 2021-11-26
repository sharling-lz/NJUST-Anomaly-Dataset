## NJUST-Anomaly Dataset

#### NJUST-Anomaly dataset contains 145 videos, including 130 training video clips and 15 testing video clips. 
The videos are taken by an unmanned aerial vehicle, leading to complex and dynamic backgrounds. Meanwhile, the video scenes  are more abundant and diverse. Events may happen on the road,  playground or lawn. Moreover, our dataset is independent of specific scenes. All of the video clips and annotations can be downloaded [here](https://pan.baidu.com/s/1TT8Qn0Q8nkhxOeY5_QaiRg). Extraction code: wpbj. 

##### Train dataset

The train dataset contains 130 training videos, and all videos are normal videos and do not contain abnormal videos.

##### Test dataset

The test dataset contains 15 videos, and some of the videos have abnormal conditions. We have given annotations for the abnormal conditions. The annotations are stored in the npy file. We store the npy files in the mask folder. And the  npy files storage format is as follows:

```python
[0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
 1 1 1 1 1 1 1 1 1 1 1]
```

0 represents a video frame under normal conditions, and 1 represents a video frame under abnormal conditions.

```
${NJUST-Anomaly data}
|-- train
    `--|--videos
       | |-- 1.mp4
       | |-- 2.mp4
       | |-- 3.mp4
       | |-- ...
`-- test
    `--|-- videos
       | |-- 1.mp4
       | |-- 2.mp4
       | |-- 3.mp4
       | |-- ... 
    `--|-- mask
       | |-- 1.npy
       | |-- 2.npy
       | |-- 3.npy
       | |-- ... 
    
```

#### Citation
If you use our dataset in your research, please cite with:

```
@inproceedings{10.1145/3444685.3446316,
author = {Tang, Yao and Zhao, Lin and Yao, Zhaoliang and Gong, Chen and Yang, Jian},
title = {Graph-Based Motion Prediction for Abnormal Action Detection},
year = {2021},
isbn = {9781450383080},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3444685.3446316},
doi = {10.1145/3444685.3446316},
booktitle = {Proceedings of the 2nd ACM International Conference on Multimedia in Asia},
articleno = {63},
numpages = {7},
keywords = {graph convolutional network, abnormal action detection, motion prediction},
location = {Virtual Event, Singapore},
series = {MMAsia '20}
}
```
