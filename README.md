## What?

Easily build linux kernel.

## How?

* Build an kernel.org linux kernel from sources
* Build a basic image to run with the kernel (debian debootsrap)
* Build and install socks related tools in the vm (dante + redsocks)
* Configure networking for MPTCP (guest + host) to use physical interfaces from the guest


## Quick start:

### Build vm (First time only)

```
source build_linux_kernel_lib

# build a debian image base. This command could last a while. And could need that you connect to Internet. You have to choose the passwd of root for the vm. If you have error "passwd no such file or directory" please restart.
build_image

# build mptcp kernel. This command clone linux kernel source to the directory linux and build and install the kernel. This command could last a while. And could need that you connect to Internet.
build_kernel

# install dante sock server (https://www.inet.no/dante/)
# install redsock server (https://darkk.net.ru/redsocks/)
# boot vm and dl/compile dante/redsocks inside the vm then shut it down (optional)
install_vm_extra

# start the vm
# if you are using ubuntu. And Enjoy
sudo su
source build_linux_kernel_lib
boot_vm
```

