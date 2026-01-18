# Linux 压缩与打包命令

## 1. tar (Tape Archive)
- **打包命令**：`tar -cvf archive.tar dir/`  
- **打包 + gzip 压缩**：`tar -czvf archive.tar.gz dir/`  
- **打包 + xz 压缩**：`tar -cJvf archive.tar.xz dir/`  
- **解压命令**：
  - gzip：`tar -xzvf archive.tar.gz -C target_dir`  
  - xz：`tar -xJvf archive.tar.xz -C target_dir`  
- **查看包内容**：
  - gzip：`tar -tzf archive.tar.gz`  
  - xz：`tar -tJf archive.tar.xz`  
- **参数说明**：
  - `c` = create
  - `x` = extract
  - `t` = list
  - `v` = verbose, 显示过程
  - `f` = 文件名
  - `z` = gzip
  - `j` = bzip2
  - `J` = xz
  - `-C` = 切换目录再解压

## 2. gzip / gunzip
- **压缩单文件**：`gzip file.txt`（会替换原文件）  
- **保留原文件**：`gzip -c file.txt > file.txt.gz`  
- **解压**：`gunzip file.txt.gz`

## 3. zip / unzip
- **打包压缩**：`zip -r archive.zip dir/`  
- **解压**：`unzip archive.zip -d target_dir`  
- **特点**：跨平台，源文件不删除，但不保留完整权限信息

## 小结
- Linux/Unix 推荐：`tar + 压缩算法`  
- 跨平台分享：`zip`
