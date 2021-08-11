# grub-install



```
sudo su

mount /dev/sda1 /mnt
mount --bind /dev /mnt/dev
mount --bind /dev/pts /mnt/dev/pts
mount --bind /proc /mnt/proc
mount --bind /sys /mnt/sys


chroot /mnt

mount boot/efi
grub-install /dev/sda
umount /boot/efi

exit

umount /mnt/dev/pts
umount /mnt/dev
umount /mnt/proc
umount /mnt/sys
umount /mnt

reboot
```
