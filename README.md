---
description: Ubuntu、Cuda 操作常用命令
---

# 常用命令

### Conda 常用命令

* **检查更新当前conda**

  Linux: `conda update conda`

* **创建虚拟环境**

  Linux: `conda create -n your_env_name python==x.x(2.7、3.6)`

  > your\_env\_name: 虚拟环境的名称， python==3.6指定python版本

* **激活虚拟环境**

  Linux: `source activate your_env_name` or `conda activate your_env_name`

* **安装包到虚拟环境**

  Linux: `conda install -n your_env_name package_name`

* **删除虚拟环境中指定的包**

  Linux: `conda remove -n your_env_name package_name`

* **退出虚拟环境**

  Linux: `source deactivate` or `conda deactivate`

* **删除虚拟环境**

  Linux: `conda remove -n your_env_name --all`

* **查看虚拟环境安装了哪些包**

  Linux: `conda list`

* **查看系统存在的虚拟环境**

  Linux: `conda env list`

* **更改 jupyter notebook kernel 路径\(虚拟环境下运行\)：**

  Linux: `pip install ipykernel`  
  Linux: `python -m ipykernel install --user --name env_name`

* **pip升级所有的包：**

  Linux: `pip freeze --local | grep -v '^-e' | cut -d = -f 1 | xargs -n1 pip install -U`

### Ubuntu 常用命令

* **显示文件系统的磁盘使用情况统计**

  Linux： `df -h`

```text
frank@312LabW:~/work$ df -h  
Filesystem      Size  Used Avail Use% Mounted on
udev            7.8G     0  7.8G   0% /dev
tmpfs           1.6G  162M  1.4G  11% /run
/dev/sda6        95G   33G   57G  37% /
tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sdb5       1.8T  605G  1.2T  35% /home
/dev/sda1       931M  445M  423M  52% /boot
```

* **显示指定文件夹的磁盘使用情况统计**

  Linux: `df /home/ -h`

```text
frank@312LabW:~/work$ df /home/ -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sdb5       1.8T  605G  1.2T  35% /home
```

* **查看CUDA版本**

  Linux: `cat /usr/local/cuda/version.txt`

* **更改用户名密码**

  Linux: `passwd 当前用户名`

  ```text
  frank@itrc:~$ passwd frank
  Changing password for frank.
  (current) UNIX password:
  Enter new UNIX password:
  Retype new UNIX password:
  ```

* **用NVIDIA GPU的deviceQuery检测一下：**

  Linux: `(keras) frank@312LabW:/usr/local/cuda/samples/1_Utilities/deviceQuery$ ./deviceQuery`

```text
./deviceQuery Starting...

 CUDA Device Query (Runtime API) version (CUDART static linking)

Detected 1 CUDA Capable device(s)

Device 0: "GeForce GTX TITAN X"
  CUDA Driver Version / Runtime Version          9.0 / 8.0
  CUDA Capability Major/Minor version number:    5.2
  Total amount of global memory:                 12206 MBytes (12798787584 bytes)
  (24) Multiprocessors, (128) CUDA Cores/MP:     3072 CUDA Cores
  GPU Max Clock rate:                            1076 MHz (1.08 GHz)
  Memory Clock rate:                             3505 Mhz
  Memory Bus Width:                              384-bit
  L2 Cache Size:                                 3145728 bytes
  Maximum Texture Dimension Size (x,y,z)         1D=(65536), 2D=(65536, 65536), 3D=(4096, 4096, 4096)
  Maximum Layered 1D Texture Size, (num) layers  1D=(16384), 2048 layers
  Maximum Layered 2D Texture Size, (num) layers  2D=(16384, 16384), 2048 layers
  Total amount of constant memory:               65536 bytes
  Total amount of shared memory per block:       49152 bytes
  Total number of registers available per block: 65536
  Warp size:                                     32
  Maximum number of threads per multiprocessor:  2048
  Maximum number of threads per block:           1024
  Max dimension size of a thread block (x,y,z): (1024, 1024, 64)
  Max dimension size of a grid size    (x,y,z): (2147483647, 65535, 65535)
  Maximum memory pitch:                          2147483647 bytes
  Texture alignment:                             512 bytes
  Concurrent copy and kernel execution:          Yes with 2 copy engine(s)
  Run time limit on kernels:                     Yes
  Integrated GPU sharing Host Memory:            No
  Support host page-locked memory mapping:       Yes
  Alignment requirement for Surfaces:            Yes
  Device has ECC support:                        Disabled
  Device supports Unified Addressing (UVA):      Yes
  Device PCI Domain ID / Bus ID / location ID:   0 / 1 / 0
  Compute Mode:
     < Default (multiple host threads can use ::cudaSetDevice() with device simultaneously) >

deviceQuery, CUDA Driver = CUDART, CUDA Driver Version = 9.0, CUDA Runtime Version = 8.0, NumDevs = 1, Device0 = GeForce GTX TITAN X
Result = PASS
```

* **查看GPU运行状态：**

  Linux:`nvidia-smi`

```text
(keras) frank@312LabW:~$ nvidia-smi
Sat Nov 17 09:18:55 2018
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 384.130                Driver Version: 384.130                   |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  GeForce GTX TIT...  Off  | 00000000:01:00.0  On |                  N/A |
| 22%   33C    P8    16W / 250W |  11928MiB / 12205MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID   Type   Process name                             Usage      |
|=============================================================================|
|    0      1627      G   /usr/lib/xorg/Xorg                           199MiB |
|    0      3403      G   compiz                                        95MiB |
|    0      7491      C   /home/wwg/.virtualenvs/cv/bin/python3      11511MiB |
|    0     22641      C   .../frank/miniconda3/envs/keras/bin/python   106MiB |
+-----------------------------------------------------------------------------+
```



