# Fire-Flyer-Record-FS

> Try to use High-Flyer AI Lab's FFRecord with DeepSeek's 3FS

## Getting Started

FFRecord depends on `libaio.h` which is Linux-specific feature

```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
sudo apt install libaio1 libaio-dev

git submodule update --init
cd submodules/ffrecord

# NOTE: either way will have bug: `ModuleNotFoundError: No module named 'ffrecord._ffrecord_cpp'` when importing `ffrecord`
python setup.py install
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -e . --force
```

> ```bash
> # BUG: ModuleNotFoundError: No module named 'pybind11'
> pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
> ```
>
> ```bash
> git submodule update --init
> pip install -i https://pypi.tuna.tsinghua.edu.cn/simple setuptools pybind11
> cd submodules/ffrecord
> # BUG (solved): Fire-Flyer-Record-FS/submodules/ffrecord/ffrecord/src/reader.cpp:13:10: fatal error: libaio.h: No such file or directory
> sudo apt install libaio1 libaio-dev
> python setup.py install
> ```

### 3FS

- [deepseek-ai/3FS: A high-performance distributed file system designed to address the challenges of AI training and inference workloads.](https://github.com/deepseek-ai/3FS)
  - [幻方力量 | 高速文件系统 3FS](https://www.high-flyer.cn/blog/3fs/)

![hardware 3fs](https://hfai-static.high-flyer.cn/static/ed76696a40254f828c34737fa07398b6/5fd3e/p0.png)

### FFRecord

- [HFAiLab/ffrecord: FireFlyer Record file format, writer and reader for DL training samples.](https://github.com/HFAiLab/ffrecord)

Dependencies

`libaio.h`:  Linux-native asynchronous I/O facility

- [Overview - libaio - Pagure.io](https://pagure.io/libaio)
- [software installation - How do I install libaio? - Ask Ubuntu](https://askubuntu.com/questions/227791/how-do-i-install-libaio)
- [libaio — Homebrew Formulae](https://formulae.brew.sh/formula/libaio)

```bash
brew install libaio
# Error: An unsatisfied requirement failed this build => libaio: Linux is required for this software.
```
