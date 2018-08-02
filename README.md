# yolo3-training-keras-master

---

## Introduction

1. use YOLOv3 training with own data
2. Compile YOLOv3 training on GPU
3. A Keras implementation of YOLOv3 detection inspired by [qqwweee/keras-yolo3](https://github.com/qqwweee/keras-yolo3).


---


## YOLOv3 training

see [YOLOv3训练自己的数据](https://blog.csdn.net/dcrmg/article/details/81296520) for details.


## YOLOv3 training with GPU

see [darknet YOLO 编译使用GPU](https://blog.csdn.net/dcrmg/article/details/78565350) for details.


## Keras implementation of YOLOv3

training with own data(rock climbers,classes of male and female)
1. Download trained YOLOv3 weights from [baidu yun](https://pan.baidu.com/s/1COD_wo_tHQfGqdrXpFMxkg).
2. Convert the Darknet YOLO model to a Keras model.
3. Run YOLO detection.

```
python convert.py ./cfg/yolov3.cfg yolov3.weights yolo.h5
python yolo.py
```


PS:
1. change value of 'self.score' in yolo.py to adjust detection threshold
2. In my case, I trained 400 epoch with 200 pictures,it is far from enough to obtain a good test result.
3. some examples:

![Alt text](https://github.com/dcrmg/yolo3-training-keras-master/blob/master/pic/01_result.jpg)

![Alt text](https://github.com/dcrmg/yolo3-training-keras-master/blob/master/pic/02_result.jpg)

![Alt text](https://github.com/dcrmg/yolo3-training-keras-master/blob/master/pic/03_result.jpg)

