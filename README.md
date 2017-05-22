# GPU-enabled Conda envs in Windows with cuda, cudnn, theano

1. Download and install CUDA from Nvidia.

2. Download the CUDNN library (version 5.1 for theano 0.9 compatibility) and copy the files into the CUDA installation directory (probably `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0`). That is, the `include/cudnn.h` file should be copied into `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\include` for example.

3. Copy the `.theanorc.txt` file from this repository into your `%USER%` directory and update as appropriate. Maybe update the `cnmem` setting if theano is using too much memory.

4. Create a new conda env using the template in this repository (theano-env.yml):
```
conda env create -f theano-env.yml
```
