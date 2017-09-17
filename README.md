# xgboost-windows
This repo contains prebuilt xgboost for windows.

## How to install xgboost python-package on windows

### Get source code

Use [Git for Windows](https://git-for-windows.github.io/)

execute this command in git bash.

    git clone -b v0.60 --recursive https://github.com/dmlc/xgboost.git

The source code will be clone to dir `xgboost`.

or download src directly [https://github.com/dmlc/xgboost/archive/v0.60.zip]

### Get built library

follow the offical [Build Guide](http://xgboost.readthedocs.io/en/latest/build.html#building-on-windows) or download the prebuilt in this repo [xgboost-v0.60-msvc-release.zip](https://github.com/fo40225/xgboost-windows/raw/master/v0.60/xgboost-v0.60-msvc-release.zip)

(my built need `vcruntime140.dll`. If you are not using Anaconda, install Microsoft Visual C++ 2015 Redistributable to get it, 2017 also works.)

Copy `libxgboost.dll` to `xgboost\python-package\xgboost\`.

### Install python package

Open command prompt with python support

change current dir to `xgboost\python-package`

install package

    python setup.py install

***

If you get the error message likes

    error: Error: setup script specifies an absolute path:

        xgboost\python-package\xgboost\libxgboost.dll

    setup() arguments must *always* be /-separated paths relative to the
    setup.py directory, *never* absolute paths.

edit `setup.py` line 19

from

    LIB_PATH = libpath['find_lib_path']()
    
to
    
    LIB_PATH = [os.path.relpath(libfile, CURRENT_DIR) for libfile in libpath['find_lib_path']()]

***

In Python interactive shell

    import xgboost as xgb
    
If there is no error message, you are ready to go.

