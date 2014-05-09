centos-packer
=============

CentOS 6.5 x86_64 + Chef 11.10 + VirtualBox 4.3.10 for Packer 0.6 Template

## Packer Build for VirtualBox

```
packer validate CentOS_6.5.json
packer build -only virtualbox-iso CentOS_6.5.json
```

## Add Vagrant Box

```
box add BOXNAME INSANEWORKS-CentOS-6.5-x86_64-v20140509.box
```

## Vagrant Cloud

```
mkdir centos
cd centos
vagrant init insaneworks/centos
vagrant up
```


## or Public URL Init

```
mkdir centos
cd centos
vagrant init INSANEWORKS-CentOS-6.5-x86_64-v20140509 http://www.insaneworks.co.jp/pub/boxes/INSANEWORKS-CentOS-6.5-x86_64-v20140509.box
vagrant up
```

## or Edit Vagrantfile (Vagrant 1.5.0 or Higher)

```diff
   # please see the online documentation at vagrantup.com.

   # Every Vagrant virtual environment requires a box to build off of.
-  config.vm.box = "base"
+  config.vm.box = "insaneworks/vagrant"

   # Create a forwarded port mapping which allows access to a specific port
   # within the machine from a port on the host machine. In the example below,
```

```
vagrant up
```

Enjoy!!
