# Fire-Flyer-Record-FS

> Try to use High-Flyer AI Lab's FFRecord with DeepSeek's 3FS

## Getting Started

FFRecord depends on `libaio.h` which is Linux-specific feature

### 3FS

- [deepseek-ai/3FS: A high-performance distributed file system designed to address the challenges of AI training and inference workloads.](https://github.com/deepseek-ai/3FS)
  - [幻方力量 | 高速文件系统 3FS](https://www.high-flyer.cn/blog/3fs/)

![hardware 3fs](https://hfai-static.high-flyer.cn/static/ed76696a40254f828c34737fa07398b6/5fd3e/p0.png)

### FFRecord

- [HFAiLab/ffrecord: FireFlyer Record file format, writer and reader for DL training samples.](https://github.com/HFAiLab/ffrecord)

Dependencies

`libaio.h`:  Linux-native asynchronous I/O facility

- [Overview - libaio - Pagure.io](https://pagure.io/libaio)
