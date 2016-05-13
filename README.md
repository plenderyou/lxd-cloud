# lxd-cloud

This project shows how to create a multi-hosted cloud with using Vagrant and virtual box.

The cloud uses an overlay layer2 network so that the lxd container share a common ip address range and dns

The cloud has 3 hosts and uses peervpn to connect them via the lxdbr0.

Lxd is already provided 

### Usage

The virtual box instances have no direct network connection but use port forwarding and so the Vagrant file requires a hostname that is available in the virtual machines.

e.g.
```
HOSTNAME=192.168.99.1
```

You also need add the ubuntu/xenial64 box

```
vagrant box add ubuntu/xenial64
```

You need to have the vagrant ansible provisioning available

Then call `vagrant up`