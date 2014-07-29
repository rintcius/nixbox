NixOS boxes for Vagrant
=======================

[NixOS](http://nixos.org) is a linux distribution based on a purely functional
package manager. This project builds .box images that can be used by
[vagrant](http://vagrantup.com), the VM manager.

Status
------

stable

Install
-------

```
vagrant init zimbat/nixbox32
# or
vagrant init zimbatm/nixbox64
```

Building the images
-------------------

First install [packer](http://packer.io) and
[virtualbox](https://www.virtualbox.org/)

Then:

```
packer build nixbox32-template.json
# or
packer build nixbox64-template.json
```

The .box image is now ready to go and you can use it in vagrant:

```
vagrant box add nixbox32 nixbox32-virtualbox.box
# or
vagrant box add nixbox64 nixbox64-virtualbox.box
```

TODO
----

There is a `vagrant-nixos` gem out there that adds a NixOS provisioning
option to vagrant. Test this out.

