# Hey! I'm Filing Here

In this lab, I successfully implemented a ext2 file system with a root and lost+found directory as well as a file with a symbolic link pointing to it.

## Building
Run this command to compile the c file into an executable, run the executable and mount the created disk image into a directory
```shell
make
./ext2-create
mkdir mnt
sudo mount -o loop cs111 -base.img mnt 
```

## Running
Run this command to check on your file system by dumping the file system information
```shell
dumpe2fs cs111-base.img
```
To check if your file system is correct you can use
```shell
fsck.ext2 cs111-base.img
```


## Cleaning up
This unmounts your file directory and remove the create directory then cleans the compiled disk image.
```shell
sudo unmount mnt
rmdir mnt
make clean
```
