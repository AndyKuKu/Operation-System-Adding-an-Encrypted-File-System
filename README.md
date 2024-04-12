# Operation-System-Adding-an-Encrypted-File-System

This project implements an encrypted file system called myext2 based on the ext2 file system in the Linux kernel. The goal is to understand the principles and implementation of file systems in Linux, particularly the Virtual File System (VFS) and ext2 file system.

Features:
- Added a new file system myext2 similar to ext2
- Modified the magic number of myext2
- Created a file system creation tool mkfs.myext2
- Implemented file encryption for read and write operations

Implementation:
- Copied the ext2 file system source code and renamed it to myext2
- Modified the magic number of myext2 to 0x6666
- Created a tool mkfs.myext2 to format a file as myext2 file system
- Added encryption/decryption functions new_sync_read_crypt and new_sync_write_crypt for file read and write operations

Usage:
- Create a file (e.g., myfs) with a specific size
- Run mkfs.myext2 myfs to format the file as myext2 file system
- Mount the file system using mount -t myext2 -o loop ./myfs /mnt
- Read and write files in the mounted directory /mnt, where data is encrypted/decrypted automatically

Notes:
- This project was implemented using the Linux kernel version 3.18.24
- The report discusses the challenges faced during the implementation and the learning experience gained from working with file systems and kernel modules.
