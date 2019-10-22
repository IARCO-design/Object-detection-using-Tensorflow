# Object detection using Tensorflow
## Background
Before we begin I think it would be best to explain my reasoning for trying out Object detection using Tensorflow.

It all started on November in the year 2018, when I came across AI and wanted to make my own project using some sort of API. Back then I did't know what AI even ment or what it was. All I knew was that it sounded cool. 

So I started off my new years resoliton with making a project that would use Tensorflow. I was so ready and exited, but it did't last long. As I started learning about neural networks and AI in general I soon realized that I wasn't good enough.

From that point on I started learning about all the math and logic needed to create neural networks to better understand how they work. I would like to say that it was easy, but it wasn't. I wen through a lot of sleepless night for weeks and moths. And after some time it all suddenly clicked.

My first experience with neural networks was with a [neural network simulator wirtten in C#](https://github.com/BeanGreen247/neural-network-simulator). That took a few months to make. After that I continued my studies on AI.

A few months have passed since then and that's where this project comes into play. I hope you enjoy it.
## Setup
### Install python
```
sudo apt install python python-dev python3.6 python3.6-dev python-tk protobuf-compiler
sudo apt install python-pip python3-pip 
```
### Upgrade setuptools
```
pip3 install --upgrade setuptools
```
### Install the dependencies
```
pip3 install tensorflow==1.5
pip3 install opencv-python
pip3 install keras
pip3 install imageAI
pip3 install matplotlib
pip3 install utils
```
### Prepare the enviroment
```
mkdir Tensorflow
cd Tensorflow
git clone https://github.com/tensorflow/models
cd models/research/
protoc object_detection/protos/*.proto --python_out=.
export PYTHONPATH=$PYTHONPATH:pwd:pwd/slim
wget http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_11_06_2017.tar.gz
wget https://raw.githubusercontent.com/BeanGreen247/Object-detection-using-Tensorflow/master/objectdetection.py
```
### Run the program from the research directory
```
python3.6 objectdetection.py
```
Let me know what you think.
