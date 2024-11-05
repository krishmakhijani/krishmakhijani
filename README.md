# LVM

1. lsblk
2. fdisk /dev/vdb ( n , p , 1 , +256M , t , 1 , 8e , w)
3. vgcreate stone /dev/vdb1 /dev/vdb2
4. vgdisplay
5. lvcreate -L 400M stone -n sand
6. mkfs -t xfs /dev/stone/sand
7. mkdir /data
8. vim /etc/fstab
9. mount /data
