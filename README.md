Singularity chainer container
=====

## Overview
This is a singularity chainer container definition file.

The building environment is included this repository. So, you can build it quickly.

## Container specifications
- OS: Ubuntu 16.04.5 LTS
- Python version: 3.5.2
- OpenCV is available

Installed python packages are below:
```sh
Singularity chainer.sif:~/development> export LC_ALL=C
Singularity chainer.sif:~/development> pip3 freeze

.... You can see the list of installed packages.
```

## Build
### Requirements
- Singularity v3.0.3
- Vagrant 2.2.3
- vagrant-disksize plugin

Your computer also have to be installed VirtualBox. It is a requirement for the Vagrant.

### Procedure
If your vagrant doesn't have vagrant-disksize plugin, please install it.

```shell
vagrant plugin install vagrant-disksize
```

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