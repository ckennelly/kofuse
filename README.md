kofuse - An Adaptive Userspace Filesystem Implementation
(c) 2013 - Chris Kennelly (chris@ckennelly.com)

Overview
========

Dynamically-loaded kernel modules offer a rich set of existing file system implementations.  Leveraging the abstractions of the kernel, from block device to file system interface, while providing basic common helper functions allows these implementations to be used by userspace programs to interpret ordinary files as entire file systems.

`kofuse` exposes the requisite stubs as to successfully link filesystem modules at runtime.  For instance, using a `vfat.ko` module and a accessible disk image, the image can be mounted and manipulated by an ordinary user (with the requisite permissions to interact with the kernel's FUSE module).

Building
========

`kofuse` relies on FUSE to expose mountable filesystems to userspace.
