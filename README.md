## NJUST-Anomaly Dataset

#### NJUST-Anomaly dataset contains 145 videos, including 130 training video clips and 15 testing video clips. 
The videos are taken by an unmanned aerial vehicle, leading to complex and dynamic backgrounds. Meanwhile, the video scenes  are more abundant and diverse. Events may happen on the road,  playground or lawn. Moreover, our dataset is independent of specific scenes. All of the video clips and annotations can be downloaded [here](https://pan.baidu.com/s/1TT8Qn0Q8nkhxOeY5_QaiRg). Extraction code: wpbj. 

##### Train set

The train set contains 130 training videos, and all videos are normal videos and do not contain abnormal videos.

##### Test set

The test set contains 15 videos, and some of the videos have abnormal conditions. We have given annotations for the abnormal conditions. The annotations are stored in the npy file. We store the npy files in the mask folder. In the npy files, the annotations are stored as follows:

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

where 0 represents a video frame under normal conditions, and 1 represents a video frame under abnormal conditions.


#### Human detection and pose estimation results
To facilitate further research, we provide human pose estimation results on the NJUST-Anomaly dataset.
We use [CenterNet](https://github.com/xingyizhou/CenterNet)+[Deep_sort](https://github.com/nwojke/deep_sort)+[PPNet](https://github.com/sharling-lz/ppnet) to get the human poses. Other human detector, multi-object tracking method, and human pose estimation method can be used.

##### Human pose in normal video
![Human pose in normal video](./pose_normal.gif)
##### Human pose in abnormal video
![Human pose in abnormal video](./pose_abnormal.gif)

#### Dataset directory
The directory of the dataset should look like as follows:
```
${NJUST-Anomaly data}
|-- train
    `--|--videos
       | |-- 1.mp4
       | |-- 2.mp4
       | |-- 3.mp4
       | |-- ...
    `--|--pose
       | |-- 1.json
       | |-- 2.json
       | |-- 3.json
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
    `--|--pose
       | |-- 1.json
       | |-- 2.json
       | |-- 3.json
       | |-- ...
    
```

