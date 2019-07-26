# Fedora CoreOS Ignition config examples

This repository contains an example of a Fedora CoreOS configuration to run a simple container using a systemd unit.

1. Download the installer ISO: https://getfedora.org/en/coreos/download/
1. Using any virtualisation software, create a VM and start the VM from the ISO
1. Press `TAB` to configure the CoreOS installer with the following kernel arguments (you may need to change the image URL to a recent release):

```
coreos.inst.install_dev=sda
coreos.inst.image_url=https://builds.coreos.fedoraproject.org/prod/streams/testing/builds/30.20190725.0/x86_64/fedora-coreos-30.20190725.0-metal.raw.xz
coreos.inst.ignition_url=https://raw.githubusercontent.com/simonkrenger/fcos-ignition-examples/master/simple-container.ign
```

As soon as the machine has rebooted, visit the following address:

```
https://<IP>:8080/random
```

## Configuration

The Ignition config was created using [fcct](https://github.com/coreos/fcct).