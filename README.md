# grub-install


`sudo su`

```mount /dev/sda1 /mnt
mount --bind /dev /mnt/dev
mount --bind /dev/pts /mnt/dev/pts
mount --bind /proc /mnt/proc
mount --bind /sys /mnt/sys

mount boot/efi

chroot /mnt

grub-install /dev/sda


exit

umount /mnt/dev/pts
umount /mnt/dev
umount /mnt/proc
umount /mnt/sys
umount /mnt
umount /boot/efi

reboot
```
