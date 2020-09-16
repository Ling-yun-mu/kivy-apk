# kivy-apk
本资源提供python打包.apk文件配置环境时所需要的所有资源。包括：kivy_deps.glew-0.2.0-cp37-cp37m-win_amd64.whl、kivy_deps.glew-0.2.0-cp37-cp37m-win_amd64.whl、kivy_deps.gstreamer-0.2.0-cp37-cp37m-win_amd64.whl、kivy_deps.sdl2-0.2.0-cp37-cp37m-win_amd64.whl、VirtualBox-4.3.12-93733-Win、Oracle_VM_VirtualBox_Extension_Pack-4.3.12-93733.vbox-extpack、kivydev.ova、以及一些工程示例。相应文章链接：https://blog.csdn.net/qq_43551034/article/details/104839917

## Recent Update
```2018.07.04```: I achieved a better accuracy(99.2%,[trained model] on LFW. I did some modification as bellow:
- Align webface and lfw dataset to ```112x112```([casia-112x112],[lfw-112x112] using [insightface align method]
- Set a bigger margin parameter (```0.35```) and a higher feature embedding demension (```1024```)
- Use the clean dataset and the details can be seen [this]
## CosFace
This project is aimmed at implementing the CosFace described by the paper [**CosFace: Large Margin Cosine Loss for Deep Face Recognition**](https://arxiv.org/pdf/1801.09414.pdf). The code can be trained on [CASIA-Webface](http://www.cbsr.ia.ac.cn/english/CASIA-WebFace-Database.html) and the best accuracy [LFW](http://vis-www.cs.umass.edu/lfw/) is 98.6%. The result is lower than reported by paper(99.33%), which may be caused by sphere network implemented in tensorflow. I train the sphere network implemented in tensorflow using the softmax loss and just obtain the accuracy 95.6%, which is more lower than caffe version(97.88%).

## Preprocessing
I supply the preprocessed dataset in baidu pan:[CASIA-WebFace-112X96] You can download and unzip them to dir ```dataset```.



## Train
```./train.sh``` 

## Test
Modify the ```MODEL_DIR``` in ```test.sh``` and run ```./test.sh```.




