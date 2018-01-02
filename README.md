# xgboost-prebuilt-wheel
This repo contains xgboost prebuilt wheel for python3.

## Windows
For the general purpose, download [this](https://github.com/fo40225/xgboost-prebuilt-wheel/tree/master/v0.7/windows/cpu/msvc/general/xgboost-0.7-py3-none-any.whl). 

    pip install xgboost-0.7-py3-none-any.whl
### msvc

need `vcopm140.dll` in PATH. If you are not using Anaconda, install Microsoft Visual C++ 2015 Redistributable [vc_redist.x64.exe](https://www.microsoft.com/en-us/download/details.aspx?id=53840) to get it, 2017 also works.

### gcc

need gcc runtime file in PATH.

### icc

Those whl are highly optimized by Intel Compiler, the folder `zen` contains cracked binary for AMD CPU.

### GPU

https://github.com/fo40225/xgboost-prebuilt-wheel/tree/master/v0.7/windows/gpu/cuda91sm30avx2

required CUDA 9.1 & compute capability 3.0 up & CPU with AVX

## mac

OpenMP enabled.

    brew install gcc6
    pip3 install xgboost-0.6-py3-none-any.whl
