kernel-ARCH-4.0.7
========

Status: DOIN
- [ ] Install my custom kernels along side the custom kernel -- contrary to most wisdom expressed on Arch forums.

Why?

- Current kernel has a compatibility issue with a machine (eg. my [Dell Inspiron Mini 1012 won't boot with kernel 4.1+](https://bugs.archlinux.org/task/47509))
- You can take the boy out of Gentoo, but you can't take Gentoo out of the boy

Issues to take care of

2. The pacman / ABC /pkgbuild for the kernel is set up to remove the kernel modules for the existing kernel when it is updated.  The LTS and mainline kernel can live side by side and the modules for both will exist in /lib/modules.

3. A problem with using older or multiple kernels occur when a package installs kernel modules and become a dependency of the kernel. E.g. *VMware* and *VirtualBox* both do this.  It is up to the user to ensure the correct kernel modules are available for those packages for their system.

Refs

[Downgrading Packages in Arch Linux: The Worst Case Scenario](https://nims11.wordpress.com/2013/02/17/downgrading-packages-in-arch-linux-the-worst-case-scenario/)
[Kernel Compilation in Arch Linux](http://www.cs.columbia.edu/~jae/4118-LAST/arch-kernel.html)
