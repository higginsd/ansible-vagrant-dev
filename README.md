----------
**Ansible Vagrant Development Environment**
===================================
----------


This vagrant environment will setup a ubuntu virtual box for ansible development ans execution, the following will be installed on the image:

 - git
 - nodejs
 - npm
 - python
 - ansible
 - aws cli
 - boto
 - azure cli


----------

Local directory sync
------------------------
By default the directory root directory where the Vagrantfile is located is synced to the /projects directory on the virtual box. to change this modify the Vagrantfile and update the dev_dir to the local directory you would like to sync

----------

Installing and running the vagrant box
----------------------------------------------

 1. download vagrant from [https://www.vagrantup.com/downloads.html](https://www.vagrantup.com/downloads.html)
 2. install the downloaded package, this should also install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
 3. open a command prompt
 4. goto the directory where you copied the Vagrantfile
 5. run "vagrant up"
 6. watch the magic happen

----------

SSH into you vagrant box
------------------------------
**On Mac OS**

 1. from the Vagrantfile directory run " vagrant ssh"

**On windows:**

 1. Install [putty](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)
 2. Convert the %USERPROFILE%\.vagrant.d\insecure_private_key to .ppk using [puttyGen](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)
 3. use the .ppk key in your PuTTY session - configured in Connection > SSH > Auth > Private key file
 4. use host 127.0.0.1
 5. use port 2222 instead of 22
 6. set the default username (vagrant) under Connection > SSH > Auth > Private key for authentication

----------

Removing the virtual box
=====================

 1. open a command prompt
 2. go to the directory where you have the Vagrantfile
 3. run "vagrant destroy"
