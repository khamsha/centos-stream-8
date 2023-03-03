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

---
# Проект по сборке CentOS Stream 8 с обновленным ядром при помощи инструментов Vagrant и Packer
Проект помогает собрать актуальный образ CentOS Stream 8 с использованием последнего стабильного ядра из репозитория elrepo-kernel. Этот образ можно легко установить как виртуальную машину на VirtualBox с помощью Vagrant.

## Подготовка
Необходимо установить VirtualBox и Oracle VM VirtualBox Extension Pack, а также `packer` и `vagrant`. Репозитории с последними доступны в [зеркале](https://hashicorp-releases.yandexcloud.net/).

## Пошаговое руководство
Начните создавать образ с помощью Packer, используя приведенную ниже команду. Следуйте инструкциям в процессе установки.
```shell
vagrant box add centos8-kernel-ml centos-8-kernel-ml-x86_64-Minimal.box
```
После успешного завершения сборки вы найдете файл `centos-8-kernel-ml-x86_64-Minimal.box` в своем рабочем каталоге.
Введите следующую команду, чтобы добавить его в Vagrant:
```shell
vagrant box add centos8-kernel-ml centos-8-kernel-ml-x86_64-Minimal.box
```
Проверьте наличие образа командой `vagrant box list`

Чтобы запустить виртуальную машину, введите команду `vagrant up`\
Подключититесь к ВМ с помощью команды `vagrant ssh`\
Сделано по мотивам задания от образовательной платформы OTUS.