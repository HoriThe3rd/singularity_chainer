Singularity chainer container
=====

## Overview
This is a singularity chainer container definition file.

The building environment is included this repository. So, you can build it quickly.

## Container specifications
- OS: Ubuntu 16.04.5 LTS
- Python version: 3.5.2

Installed python packages are below:
```sh
Singularity chainer.sif:~/development> export LC_ALL=C
Singularity chainer.sif:~/development> pip3 freeze

chainer==6.0.0b2
cupy-cuda92==6.0.0b2
cycler==0.10.0
fastrlock==0.4
filelock==3.0.10
kiwisolver==1.0.1
matplotlib==3.0.2
numpy==1.16.0
opencv-python==4.0.0.21
pandas==0.24.1
protobuf==3.6.1
pyparsing==2.3.1
python-dateutil==2.8.0
pytz==2018.9
scikit-learn==0.20.2
scipy==1.2.1
six==1.12.0
tqdm==4.31.1
typing==3.6.6
typing-extensions==3.7.2
```

## Build
### Requirements
- Singularity v3.0.3
- Vagrant 2.2.3

Your computer also have to be installed VirtualBox. It is a requirement for the Vagrant.

### Procedure
To build the container, you run the commands as shown below.

Note: All commands have to be executed in top directory of this repository.
```sh
# Setup the virtual machine
vagrant up
# Enter the VM's shell
vagrant ssh

# Build the container
sudo singularity build chainer.sif chainer.def

# After execution the command, you can see the chainer.sif which is the container
```