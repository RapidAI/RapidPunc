A library for adding punctuations into a piece of text getting from an ASR.

## Build on Linux X64

git clone  https://github.com/RapidAI/RapidPunc.git

cd RapidPunc

mkdir build

cd build

\# dowload onnxruntime:

wget https://github.com/microsoft/onnxruntime/releases/download/v1.14.1/onnxruntime-linux-x64-1.14.1.tgz



tar zxf  onnxruntime-linux-x64-1.14.1.tgz

 cmake -DONNXRUNTIME_DIR=/data/linux/FunASR/funasr/runtime/rapidpunc/build/onnxruntime-linux-x64-1.14.1 ..

make -j16



Then get two files: 

librapidpunc.so   

rapidpunc_tester



## Download model

```
链接：https://pan.baidu.com/s/1neFfd6HT4PLvvqeixxvH2w?pwd=y85r 
提取码：y85r
```

## Run

rapidpunc_tester /path/to/model/dir  /path/to/wave/file



in a model_dir, it should include: punc.yaml  model.onnx

