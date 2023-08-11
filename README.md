# rhel-boot-kernel-order

Change the order of the kernel model in rhel:

Check all the kernel:

```bash
grubby --info=ALL | grep title
```

Index are assigned in ascending order i.e. kernel name at the top will be given 0 index and then below it will be given 1,2 and 3,etc.

Check the default kernel:

```bash
grubby --default-kernel
```

Check the default kernel index:

```bash
grubby --default-index
```

Finally change the default kernel by giving its index:
In my case i will give index 0(as it is rtk kernel and i want to make it default)

```bash
grub2-set-default 0
```

Give any other number if you dont want the kernel at index 0

Now reboot the system:

```bash
sudo reboot
```

After rebooting:
Check the kernel 

```bash
uname -r
```
