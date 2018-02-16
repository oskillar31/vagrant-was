# vagrant-websphere

## Description
Vagrantfile to create an Ubuntu (trusty64) Virtual Machine using **Vagrant**, and provision it using **Ansible** playbook.

Ansible will install trial version (60 days) of IBM WebSphere Application Server 8.5. Once license is expired you wont be able to use it anymore, then you can destroy de virtual machine and `vagrant up` a new one :)

WebSphere Application server instance will contain a cell formed by:
* 1 x Deployment Manager
* 1 x Node agent
* 1 x Application Server with an example application (PlantsByWebSphere).

## System requirements
* Internet connection (IBM Installation Manager needs to download files).
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads) 5.1.X
* [Vagrant](https://www.vagrantup.com/downloads.html) 2.X

## Prerequisites
* Download [NDTRIAL.agent.installer.linux.gtk.x86_64.zip](https://drive.google.com/uc?export=download&id=0B-Az43g0UG4hRl84dnFSOGxIbDA) and put it into "files" folder.

## Installation instructions
1. Clone this repository

    ```bash
    $ git clone git@github.dxc.com:mmenendezvaz/vagrant-websphere.git
    ```

2. Download [NDTRIAL.agent.installer.linux.gtk.x86_64.zip](https://drive.google.com/uc?export=download&id=0B-Az43g0UG4hRl84dnFSOGxIbDA) and place it into `files` directory.

3. Change to repository root folder and run `vagrant up` to create and provision the VM.

    ```bash
    $ cd vagrant-websphere
    $ vagrant up
    ```
