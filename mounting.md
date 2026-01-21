# 挂载与 /etc/fstab

## 挂载命令
- `mount /dev/sr0 /mnt/cdrom`：挂载光盘到目录
- `umount /mnt/cdrom`：卸载

## /etc/fstab 文件
- 系统启动时自动挂载设备
- 每行格式：
  1. 设备名（/dev/sda1, /dev/cdrom）
  2. 挂载点（/mnt/data, /mnt/cdrom）
  3. 文件系统类型（ext4, xfs, iso9660）
  4. 挂载选项（defaults, ro, rw）
  5. dump（是否备份，一般 0）
  6. fsck 顺序（检查顺序，一般 0 或 1）

## 示例
/dev/cdrom /mnt/cdrom iso9660 defaults 0 0
/dev/sda1 /mnt/data ext4 defaults 0 1
- iso9660：光盘文件系统，只读
- ext4/xfs：Linux 硬盘文件系统，可读写
 
