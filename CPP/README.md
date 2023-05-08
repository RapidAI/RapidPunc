## RapidPunc
- A library for adding punctuations into a piece of text getting from an ASR.
- 用于对ASR识别后的结果添加标点符号。
- 模型来自于阿里达摩院。

### Build on Linux X64
- make
    ```bash
    git clone  https://github.com/RapidAI/RapidPunc.git
    cd RapidPunc/CPP
    mkdir build
    cd build
    \# dowload onnxruntime:

    wget https://github.com/microsoft/onnxruntime/releases/download/v1.14.1/onnxruntime-linux-x64-1.14.1.tgz

    tar zxf  onnxruntime-linux-x64-1.14.1.tgz

    cmake -DONNXRUNTIME_DIR=/data/linux/FunASR/funasr/runtime/rapidpunc/build/onnxruntime-linux-x64-1.14.1 ..

    make -j16
    ```

- Then get two files:
    ```bash
    librapidpunc.so
    rapidpunc_tester
    ```

### Download model
- [百度网盘](https://pan.baidu.com/s/1neFfd6HT4PLvvqeixxvH2w?pwd=y85r)

### Run
```bash
rapidpunc_tester /path/to/model/dir  /path/to/wave/file
```

in a model_dir, it should include:
```text
punc.yaml
model.onnx
```

### Example
[Tester.cpp](./sources/tester.cpp)
