# 分区操作与格式

## 分区概念
- 一个磁盘可以分为多个逻辑分区
- 常用分区工具：
  - `fdisk /dev/sda`（MBR 分区）
  - `parted /dev/sda`（GPT 分区）

## 分区格式化
- `mkfs.ext4 /dev/sda1`：格式化为 ext4
- `mkfs.xfs /dev/sda2`：格式化为 xfs
- 光盘无需格式化，直接使用 iso9660
