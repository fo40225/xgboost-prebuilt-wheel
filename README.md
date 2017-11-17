# xgboost-prebuilt
This repo contains prebuilt xgboost for python3.

## Windows
For the general purpose, download [this](https://github.com/fo40225/xgboost-prebuilt/raw/master/v0.60/windows/msvc/general/xgboost-0.6-py3-none-any.whl). 

    pip install xgboost-0.6-py3-none-any.whl
### msvc

need `vcopm140.dll` in PATH. If you are not using Anaconda, install Microsoft Visual C++ 2015 Redistributable [vc_redist.x64.exe](https://www.microsoft.com/en-us/download/details.aspx?id=53840) to get it, 2017 also works.

### gcc

need gcc 6 runtime file in PATH.

### icc

Those whl are highly optimized by Intel Compiler, the folder `zen` contains cracked binary for AMD CPU.

## mac

OpenMP enabled.

    brew install gcc6
    pip3 install xgboost-0.6-py3-none-any.whl
