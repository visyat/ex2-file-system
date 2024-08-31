# Hey! I'm Filing Here

In this lab, I successfully implemented a 1 MiB ext2 file system with 2 directories, 1 regular file, and 1 symbolic link. 

## Building
Run the following code to build the necessary `ext2-create` executable
```
make
```

## Running
Run the following commands to run the executable and mount the resulting file system image. 
```
./ext2-create
dumpe2fs cs111-base.img
fsck.ext2 cs111-base.img
mkdir mnt
sudo mount -o loop cs111 -base.img mnt
```

## Cleaning up
When done, run the following code to unmount the file system and delete the unecessary directories and binary files. 
```
sudo umount mnt
rmdir mnt
make clean
```
