# Vagrant Melting pot
This is a collection of the Vagrant files I use for day-to-day work, testing and other such things...

## Prerequisites
The following plugins are recommended:
* vagrant-hostmanager
* vagrant-hosts
* vagrant-multi-putty (for Windows hosts)
These can be deployed via vagrant's plugin manager:
```bash
vagrant plugin install vagrant-hostmanager vagrant-hosts vagrant-multi-putty
```

## Usage
To use a template, copy the template of your choice to a working directory and rename it to vagrantfile.
```bash
cp Vagrantfile_nginxdemo /tmp/vagrantfile
cd /tmp
vagrant up
```

## Vagrant templates

### For temporary lab workstations
* Vagrantfile_workstation: Windows 7 image based on dealertrack/IE11-Win7 (and choice of other modern-ie systems), increases winrm concurrent ops, auto-deploys mRemoteNG, pre-saved connections, drops shortcut on desktop and updates host file

### For Presentations/Training sessions
* Vagrantfile_nginxdemo: Chef & nginx deployment/configuration for training/presentations

### Base images
* Vagrantfile_modern-ie-vagrant: my fork of modern-ie from https://github.com/markhuber/modern-ie-vagrant, performs winrm call to increase concurrent ops
* Vagrantfile_Ubuntu_Trusty: deploys a Ubuntu 14.04.4 (LTS) Trusty image
* Vagrantfile_2008R2: deploys a Windows 2008 R2 Server based on opentable/win-2008r2-standard-amd64-nocm
* Vagrantfile_2012R2: deploys a Windows 2012 R2 Server based on opentable/win-2012r2-standard-amd64-nocm

### modern-ie-vagrant/workstation Boxes

* EdgeOnWindows10
* IE11onWin8.1
* Win7.1
