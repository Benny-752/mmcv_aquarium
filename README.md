# README



## Steps to Train

***Ensure that you have installed MMCV and MMDetection before proceeding with the following steps.***

* Clone the [MMDetection](https://github.com/open-mmlab/mmdetection.git) repository.

```
git clone https://github.com/open-mmlab/mmdetection.git
```

* Download the weights weights.

```
python download_weights.py --weights yolov3_d53_320_273e_coco
```

* Prepare the dataset in the Pascal VOC directory structure.

```
python prepare_voc_format.py
```

* Train the model.

```
python train.py 
```

* Inference on images.

```
python inference_image.py --weights outputs/yolov3_d53_320_273e_coco/epoch_100.pth --threshold 0.25
```

* Inference on videos.

```
python inference_video.py --weights outputs/yolov3_d53_320_273e_coco/epoch_100.pth --input input/inference_data/video_1.mp4 --threshold 0.25
```

```
python inference_video.py --weights outputs/yolov3_d53_320_273e_coco/epoch_100.pth --input input/inference_data/video_2.mp4 --threshold 0.25
```



## Image / Video Credits and Attributions

* `input/inference_data/`
  * `video_1.mp4`:  Video by Magda Ehlers: https://www.pexels.com/video/underwater-footage-2556894/.
    * https://www.pexels.com/video/underwater-footage-2556894/
  * `video_2.mp4`: Video by Sébastien Vincon: https://www.pexels.com/video/stingray-swimming-underwater-10372904/.
    * https://www.pexels.com/video/stingray-swimming-underwater-10372904/
  * 
