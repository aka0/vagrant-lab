## Description
Vagrantfile for my lab machines in VirtualBox

## Machine Listing

All machines start with 2048MB ram and 2 CPUs.

### REMNux
LAB-REMNux
- Ubuntu 20.04
- See [REMNux documentation](https://docs.remnux.org/)

### FlareVM
LAB-FlareVM
- Windows 10
- See [FlareVM documentation](https://github.com/mandiant/flare-vm)

## Networking
DHCP Host-Only Network (VirtualBox default)
- 192.168.56.0/24

All VMs will have Internet access upon creation.

*Important*
Please make sure network is configured properly (e.g. isolated) prior to malware detonation.

## Known Issue
- Vagrant is unable to connect to FlareVM if `private_network` and static ip (host-only network) is used.
