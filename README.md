# CentOS Stream 8 Vagrant+Packer project with kernel updating script
The project helps to build up-to-date CentOS Stream 8 image using latest stable kernel from elrepo-kernel repository. This image can be easily installed as VM on VirtualBox with Vagrant.

## Prerequisites
You need VirtualBox and Oracle VM VirtualBox Extension Pack to be installed on a workstation.
Also install `packer` and `vagrant` using your package manager or download repositories from the [mirror](https://hashicorp-releases.yandexcloud.net/).

## Step-by-step guide
Start building an image with Packer using the command below. Follow instructions during installation process.
```shell
packer build centos.json
```
Once build is successfully completed you'll find `centos-8-kernel-ml-x86_64-Minimal.box` file in your working directory.
Enter the following command to add it to Vagrant:
```shell
vagrant box add centos8-kernel-ml centos-8-kernel-ml-x86_64-Minimal.box
```
Check new image in `vagrant box list`

In order to start VM type `vagrant up` command.\
You can connect to your VM using `vagrant ssh` command.