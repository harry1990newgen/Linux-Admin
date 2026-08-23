

Author : Harry Singh
Modified : 23Aug2026

This covers Basic System Navigation, file management, user/process handling, networking, services, logs, disk management, permissions, troubleshooting, and basic shell scripting.

## 📑 Table of Contents

1. [Basic System Navigation](#-1-basic-system-navigation)
2. [File Permissions & Ownership](#-2-file-permissions--ownership)
3. [User & Group Management](#-3-user--group-management)
4. [Process & System Monitoring](#-4-process--system-monitoring)
5. [Disk, Filesystem & Storage](#-5-disk-filesystem--storage)
6. [Networking & Connectivity](#-6-networking--connectivity)
7. [System Services & Startup](#-7-system-services--startup)
8. [Logs & Troubleshooting](#-8-logs--troubleshooting)
9. [Package Management](#-9-package-management)
10. [Compression & Archiving](#-10-compression--archiving)
11. [File Viewing & Editing](#-11-file-viewing--editing)
12. [Shell & Scripting Basics](#-12-shell--scripting-basics)
13. [System Information](#-13-system-information)
14. [Interview-Focused Practical Topics](#-14-interview-focused-practical-topics)
15. [Quick Revision Checklist](#-quick-revision-checklist-for-l0l1-interviews)
16. [Linux Command Quick Reference](#-linux-command-quick-reference-chart)
17. [Top Practical Tasks](#-top-10-practical-tasks-for-l0l1-interviews)
18. [Linux Practical Tasks](#-linux-practical-tasks-for-l0l1--support-engineer-interviews)
19. [Linux Boot Process & Troubleshooting](#-linux-boot-related-issues--tasks)

---

# 🐧 Linux Commands, Practical Tasks & Interview Guide

## 🧩 1. Basic System Navigation

## 🧠 2. File Permissions & Ownership

## 🧍 3. User & Group Management

## ⚙️ 4. Process & System Monitoring

## 💾 5. Disk, Filesystem & Storage

## 🌐 6. Networking & Connectivity

## 🔥 7. System Services & Startup

## 📜 8. Logs & Troubleshooting

## 🧰 9. Package Management

## 🧱 10. Compression & Archiving

## 🧩 11. File Viewing & Editing

## 🕹️ 12. Shell & Scripting Basics

## 🧭 13. System Information

## 🧰 14. Interview-Focused Practical Topics

## 🧾 15. Quick Revision Checklist for L0/L1 Interviews

## 🧩 16. Linux Command Quick Reference Chart

## 🎯 17. Top 10 Practical Tasks for L0/L1 Interviews

## 🧩 18. Linux Practical Tasks for L0/L1 / Support Engineer Interviews

## ⚙️ 19. Linux Boot Related Issues & Tasks



🧩 1. Basic System Navigation :

| Command                        | Description                                                 |
| ------------------------------ | ----------------------------------------------------------- |
| `pwd`                          | Show current working directory                              |
| `ls -l`, `ls -a`, `ls -lh`     | List files with details, hidden files, human-readable sizes |
| `cd`, `cd ..`, `cd /`          | Change directories                                          |
| `mkdir`, `rmdir`               | Create / remove directories                                 |
| `touch`, `cat`, `more`, `less` | Create/view files                                           |
| `cp`, `mv`, `rm`               | Copy, move, delete files                                    |
| `find / -name filename`        | Search for files                                            |
| `locate filename`              | Quick search using database                                 |
| `file filename`                | Determine file type                                         |
| `head`, `tail`, `tail -f`      | Show start/end of files; follow log updates                 |

🧠 2. File Permissions & Ownership :

| Command                 | Description                     |
| ----------------------- | ------------------------------- |
| `chmod 755 file`        | Change file permissions         |
| `chown user:group file` | Change owner and group          |
| `umask`                 | Show or set default permissions |
| `ls -ld dirname`        | Check directory permissions     |


🧍 3. User and Group Management : 

| Command                                 | Description                      |
| --------------------------------------- | -------------------------------- |
| `useradd username` /                    | Add new user                     |
| `passwd username`                       | Set password                     |
| `usermod -aG group username`            | Add user to group                |
| `groupadd groupname`                    | Create group                     |
| `id username`                           | Show user’s UID, GID, and groups |
| `whoami`, `who`, `w`                    | Show current or logged-in users  |
| `su - user`, `sudo command`             | Switch user / run as root        |

⚙️ 4. Process and System Monitoring : 

| Command                            | Description                  |
| ---------------------------------- | ---------------------------- |
| `ps -ef`                           | Show all running processes   |
| `top`, `htop`                      | Live system resource monitor |
| `kill -9 PID`, `pkill processname` | Kill process by PID or name  |
| `nice`, `renice`                   | Adjust process priority      |
| `free -m`                          | Show memory usage            |
| `uptime`                           | Show system load and uptime  |
| `vmstat`, `iostat`, `sar`          | Performance statistics       |


💾 5. Disk, Filesystem, and Storage : 

| Command                 | Description                    |
| ----------------------- | ------------------------------ |
| `df -h`                 | Disk space usage               |
| `du -sh *`              | Directory size summary         |
| `lsblk`                 | List block devices             |
| `fdisk -l`, `parted -l` | Partition information          |
| `mount`, `umount`       | Mount/Unmount devices          |
| `blkid`, `fstab`        | Disk UUIDs / persistent mounts |
| `swapoff`, `swapon`     | Manage swap space              |

🌐 6. Networking & Connectivity :

| Command                       | Description               |
| ----------------------------- | ------------------------- |
| `ip a`, `ifconfig`            | Show network interfaces   |
| `ping`, `traceroute`, `mtr`   | Test network connectivity |
| `netstat -tulnp`, `ss -tulnp` | Show listening ports      |
| `nslookup`, `dig`             | DNS resolution            |
| `scp`, `sftp`                 | Secure file transfer      |
| `ssh user@host`               | Remote login              |
| `hostnamectl`                 | Show or set hostname      |
| `curl`, `wget`                | Download data from web    |


🔥 7. System Services & Startup :

| Command                                    | Description             |
| ------------------------------------------ | ----------------------- |
| `systemctl status servicename`             | Check service status    |
| `systemctl start/stop/restart servicename` | Manage services         |
| `systemctl enable/disable servicename`     | Start service at boot   |
| `journalctl -u servicename`                | Show logs for a service |
| `service servicename status`               | Legacy service command  |
| `chkconfig`, `update-rc.d`                 | SysV service management |


📜 8. Logs and Troubleshooting :

| Command                 | Description                    |                 |
| ----------------------- | ------------------------------ | --------------- |
| `dmesg                  | tail`                          | Kernel messages |
| `journalctl`            | System logs (RHEL7+ / systemd) |                 |
| `cat /var/log/messages` | General system logs            |                 |
| `cat /var/log/secure`   | Authentication logs            |                 |
| `grep`, `awk`, `sed`    | Filter and parse logs          |                 |
| `less /var/log/syslog`  | View log files interactively   |                 |


🧰 9. Package Management :

| OS                        | Commands                                             |
| ------------------------- | ---------------------------------------------------- |
| **RHEL / CentOS / Rocky** | `yum`, `dnf`, `rpm -qa`, `dnf install`, `dnf update` |
| **Debian / Ubuntu**       | `apt-get`, `apt-cache`, `dpkg -l`, `apt install`     |


🧱 10. Compression & Archiving :

| Command                    | Description         |
| -------------------------- | ------------------- |
| `tar -cvf backup.tar /dir` | Create tar archive  |
| `tar -xvf backup.tar`      | Extract tar archive |
| `gzip`, `gunzip`           | Compress/Decompress |
| `zip -r`, `unzip`          | Zip/Unzip           |


🧩 11. File Viewing & Editing :

| Command                             | Description           |
| ----------------------------------- | --------------------- |
| `cat`, `tac`                        | Display file contents |
| `grep 'word' file`                  | Search in file        |
| `sort`, `uniq`, `cut`, `awk`, `sed` | Text manipulation     |
| `vi`, `nano`                        | File editing tools    |


🕹️ 12. Shell & Scripting Basics

| Command / Concept                    | Description            |
| ------------------------------------ | ---------------------- |
| `#!/bin/bash`                        | Script shebang         |
| `echo`, `read`, `if`, `for`, `while` | Basic scripting        |
| `date`, `whoami`, `uname -r`         | Useful system info     |
| `crontab -e`, `at`                   | Schedule jobs          |
| `alias`, `history`, `export`         | Environment management |


🧭 13. System Information :

| Command                            | Description               |
| ---------------------------------- | ------------------------- |
| `uname -a`                         | Kernel and OS info        |
| `cat /etc/os-release`              | Linux distribution info   |
| `lscpu`, `lsmem`, `lsusb`, `lspci` | Hardware info             |
| `dmidecode`                        | Detailed hardware details |
| `who -b`                           | Last system boot time     |


🧰 14. Interview-Focused “Practical” Topics

How to check service status (systemctl status httpd)
How to add a new user with sudo privileges
How to check which port a service uses
How to analyze log file for errors (grep -i error /var/log/messages)
How to check CPU/memory usage
How to find large files (du -ahx / | sort -rh | head -20)
How to schedule and verify cron jobs
How to check disk utilization
How to troubleshoot network issue (ping, nslookup, ss -tulnp)

🧾 Bonus: Quick Revision Checklist for L0/L1 Interviews

✅ Linux boot process (GRUB → init/systemd)
✅ Runlevels / targets (systemctl get-default)
✅ User management & sudoers file
✅ File permissions & sticky bit
✅ Basic troubleshooting (logs, top, ps)
✅ Package install/update/remove
✅ Service management
✅ Network diagnostics
✅ Crontab setup
✅ Mount/unmount disks
✅ Difference between hard link and soft link


🧩 Linux Command Quick Reference Chart (L0/L1 Support) : 
| 🏷️ Category                | 💻 Command(s)                                                        | 🧠 Purpose / Description                 | 🧾 Example                               |
| --------------------------- | -------------------------------------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| **System Info**             | `uname -a`, `hostnamectl`, `uptime`, `whoami`                        | Check OS, hostname, uptime, current user | `uname -a`                               |
| **Navigation**              | `pwd`, `cd`, `ls -l`, `tree`                                         | Show current dir, move, list files       | `ls -lh /var`                            |
| **File Handling**           | `cat`, `touch`, `cp`, `mv`, `rm`, `file`                             | Create, copy, move, delete files         | `cp file1 /tmp/`                         |
| **Directory Handling**      | `mkdir`, `rmdir`, `find`, `locate`                                   | Create/remove/search directories         | `find / -name passwd`                    |
| **Viewing Files**           | `cat`, `more`, `less`, `head`, `tail`, `tail -f`                     | Display file content                     | `tail -f /var/log/messages`              |
| **Text Filters**            | `grep`, `awk`, `sed`, `sort`, `uniq`, `cut`                          | Filter/search/format text                | `grep error /var/log/syslog`             |
| **Links**                   | `ln file hardlink`, `ln -s file symlink`                             | Create hard/soft links                   | `ln -s /etc/passwd pfile`                |
| **Permissions**             | `chmod`, `chown`, `chgrp`, `umask`                                   | Manage file permissions & ownership      | `chmod 755 script.sh`                    |
| **Users & Groups**          | `useradd`, `passwd`, `usermod`, `id`, `groups`, `who`                | Manage users & groups                    | `usermod -aG wheel user1`                |
| **Process Mgmt**            | `ps -ef`, `top`, `htop`, `kill`, `nice`, `renice`, `pgrep`           | Monitor/kill processes                   | `kill -9 1234`                           |
| **System Monitoring**       | `vmstat`, `iostat`, `sar`, `free -m`, `uptime`, `dmesg`              | Check CPU, memory, I/O                   | `free -h`                                |
| **Disk Mgmt**               | `df -h`, `du -sh *`, `lsblk`, `fdisk -l`, `mount`, `umount`          | Check/Manage disk usage                  | `df -Th`                                 |
| **Swap Mgmt**               | `swapon -s`, `swapoff`, `mkswap`                                     | Manage swap space                        | `swapon /dev/sdb1`                       |
| **File Systems**            | `mkfs`, `blkid`, `mount`, `cat /etc/fstab`                           | Create/mount filesystems                 | `mount /dev/sdb1 /mnt`                   |
| **Archiving & Compression** | `tar`, `gzip`, `gunzip`, `zip`, `unzip`                              | Compress/uncompress files                | `tar -czvf backup.tar.gz /home`          |
| **Package Mgmt (RHEL)**     | `yum`, `dnf`, `rpm -qa`                                              | Install/update packages                  | `dnf install httpd`                      |
| **Package Mgmt (Debian)**   | `apt-get`, `apt-cache`, `dpkg -l`                                    | Debian/Ubuntu package tools              | `apt install nginx`                      |
| **Service Mgmt (Systemd)**  | `systemctl start/stop/status`, `enable`, `disable`                   | Manage services                          | `systemctl status sshd`                  |
| **Networking**              | `ip a`, `ping`, `traceroute`, `ss -tulnp`, `netstat`, `curl`, `wget` | Network info & connectivity              | `ping 8.8.8.8`                           |
| **DNS Tools**               | `nslookup`, `dig`, `host`                                            | DNS query testing                        | `dig google.com`                         |
| **Remote Access**           | `ssh`, `scp`, `sftp`                                                 | Connect to remote hosts / transfer files | `scp file user@host:/tmp/`               |
| **Logs & Troubleshooting**  | `cat /var/log/messages`, `journalctl`, `dmesg`, `grep`               | Analyze system logs                      | `grep fail /var/log/secure`              |
| **Scheduling Jobs**         | `crontab -e`, `at`, `systemctl list-timers`                          | Schedule automated jobs                  | `crontab -l`                             |
| **System Startup**          | `systemctl get-default`, `reboot`, `shutdown`, `runlevel`            | Control boot/run levels                  | `systemctl isolate multi-user.target`    |
| **Hardware Info**           | `lscpu`, `lspci`, `lsusb`, `dmidecode`, `hwinfo`                     | Hardware details                         | `lscpu`                                  |
| **Memory Info**             | `free -m`, `vmstat`, `cat /proc/meminfo`                             | Check memory usage                       | `free -m`                                |
| **Performance Check**       | `sar`, `iostat`, `mpstat`                                            | Historical performance                   | `sar -u 5 5`                             |
| **System Update**           | `dnf update`, `apt upgrade`                                          | Apply updates                            | `dnf update -y`                          |
| **Security**                | `sudo`, `visudo`, `passwd`, `last`, `w`, `who`                       | Manage access and users                  | `sudo vi /etc/sudoers`                   |
| **Disk Check & Repair**     | `fsck`, `e2fsck`, `tune2fs`                                          | Check & fix filesystem errors            | `fsck /dev/sda1`                         |
| **Boot & Grub**             | `grub2-mkconfig`, `grub2-install`, `systemctl get-default`           | Bootloader & runlevel                    | `grub2-mkconfig -o /boot/grub2/grub.cfg` |
| **Backup**                  | `rsync`, `scp`, `tar`, `cp -r`                                       | Backup or sync data                      | `rsync -avz /data /backup/`              |
| **Environment**             | `env`, `export`, `set`, `alias`, `history`                           | Manage environment variables             | `export PATH=$PATH:/opt/bin`             |
| **Scripting Basics**        | `#!/bin/bash`, `if`, `for`, `while`, `echo`, `read`                  | Automate tasks                           | `echo "Hello Linux!"`                    |


🎯 Top 10 Practical Tasks for L0/L1 Interviews : 
| Task                                 | Relevant Commands                               |          |           |
| ------------------------------------ | ----------------------------------------------- | -------- | --------- |
| Check system uptime, CPU, and memory | `uptime`, `top`, `free -m`                      |          |           |
| Restart a failed service             | `systemctl restart httpd`                       |          |           |
| Find a large file eating disk space  | `du -ahx /                                      | sort -rh | head -10` |
| Monitor logs for errors              | `tail -f /var/log/messages`                     |          |           |
| Check which ports are open           | `ss -tulnp`                                     |          |           |
| Add user with sudo                   | `useradd user1`, `usermod -aG wheel user1`      |          |           |
| Verify network connectivity          | `ping`, `curl`, `nslookup`                      |          |           |
| Schedule a cron job                  | `crontab -e`                                    |          |           |
| Mount an extra disk                  | `mount /dev/sdb1 /mnt`                          |          |           |
| Check process consuming high CPU     | `top` / `ps -eo pid,comm,%cpu,%mem --sort=-%cpu | head`    |           |

🧩 Linux Practical Tasks for L0/L1 / Support Engineer Interviews :

⚙️ 1. System Information & Basic Ops
| 🔢 Task | 🧠 Objective                       | 💻 Command Example    |
| ------- | ---------------------------------- | --------------------- |
| 1       | Check Linux version                | `cat /etc/os-release` |
| 2       | Check kernel version               | `uname -r`            |
| 3       | Check hostname                     | `hostnamectl`         |
| 4       | Display current date/time          | `date`                |
| 5       | Find system uptime                 | `uptime`              |
| 6       | Display current users              | `who`, `w`            |
| 7       | Check system architecture          | `arch` or `uname -m`  |
| 8       | List logged-in users and their IPs | `who -uH`             |


📁 2. File and Directory Management
| 🔢 Task | 🧠 Objective                      | 💻 Command Example                         |
| ------- | --------------------------------- | ------------------------------------------ |
| 9       | Create nested directories         | `mkdir -p /opt/projects/demo`              |
| 10      | Copy directory recursively        | `cp -r /src /backup/`                      |
| 11      | Move files to another folder      | `mv *.log /tmp/`                           |
| 12      | Delete files older than 10 days   | `find /var/log -type f -mtime +10 -delete` |
| 13      | Find and list large files         | `find / -type f -size +500M`               |
| 14      | View file content with pagination | `less /etc/passwd`                         |
| 15      | Compare two files                 | `diff file1 file2`                         |
| 16      | Count number of lines in a file   | `wc -l /var/log/messages`                  |


👥 3. User & Group Management
| 🔢 Task | 🧠 Objective                | 💻 Command Example                      |
| ------- | --------------------------- | --------------------------------------- |
| 17      | Create a new user           | `useradd user1`                         |
| 18      | Set user password           | `passwd user1`                          |
| 19      | Create a new group          | `groupadd support`                      |
| 20      | Add user to group           | `usermod -aG support user1`             |
| 21      | Lock or unlock user account | `usermod -L user1` / `usermod -U user1` |
| 22      | Check user details          | `id user1`                              |
| 23      | Change file ownership       | `chown user1:group1 file.txt`           |
| 24      | Check last login time       | `lastlog`                               |



🧰 4. File Permissions
| 🔢 Task | 🧠 Objective                  | 💻 Command Example                       |
| ------- | ----------------------------- | ---------------------------------------- |
| 25      | View permissions              | `ls -l`                                  |
| 26      | Change file permission        | `chmod 755 script.sh`                    |
| 27      | Change ownership              | `chown root:root file.txt`               |
| 28      | Set sticky bit on a directory | `chmod +t /shared`                       |
| 29      | Set SGID/SetUID               | `chmod g+s dir` or `chmod u+s /bin/ping` |
| 30      | Check effective permissions   | `namei -l /path/to/file`                 |


🧠 5. Process & Resource Monitoring
| 🔢 Task | 🧠 Objective                       | 💻 Command Example                 |          |
| ------- | ---------------------------------- | ---------------------------------- | -------- |
| 31      | Show all processes                 | `ps -ef`                           |          |
| 32      | Find process by name               | `pgrep httpd`                      |          |
| 33      | Kill a process                     | `kill -9 PID`                      |          |
| 34      | Check CPU usage                    | `top` or `mpstat`                  |          |
| 35      | Check memory usage                 | `free -m`                          |          |
| 36      | Find top 5 memory-hungry processes | `ps -eo pid,comm,%mem --sort=-%mem | head -6` |
| 37      | Display load average               | `uptime`                           |          |
| 38      | Monitor real-time logs             | `tail -f /var/log/messages`        |          |


💾 6. Disk & Filesystem Management
| 🔢 Task | 🧠 Objective                      | 💻 Command Example     |
| ------- | --------------------------------- | ---------------------- |
| 39      | Check disk usage                  | `df -h`                |
| 40      | Check partition layout            | `lsblk`                |
| 41      | Mount a partition                 | `mount /dev/sdb1 /mnt` |
| 42      | Unmount a partition               | `umount /mnt`          |
| 43      | Add entry to fstab                | `vi /etc/fstab`        |
| 44      | Check inode usage                 | `df -i`                |
| 45      | Check available space in a folder | `du -sh /var/log/`     |
| 46      | Find filesystem type              | `df -T` or `blkid`     |


🌐 7. Networking Tasks
| 🔢 Task | 🧠 Objective              | 💻 Command Example             |
| ------- | ------------------------- | ------------------------------ |
| 47      | Display IP address        | `ip a`                         |
| 48      | Test network connectivity | `ping 8.8.8.8`                 |
| 49      | Check open ports          | `ss -tulnp`                    |
| 50      | Verify DNS resolution     | `nslookup google.com`          |
| 51      | Download file from URL    | `wget http://example.com/file` |
| 52      | Copy file over SSH        | `scp file user@host:/path/`    |
| 53      | Test SSH connectivity     | `ssh user@server`              |
| 54      | Check routing table       | `ip route`                     |


🔥 8. Service & Daemon Management
| 🔢 Task | 🧠 Objective                 | 💻 Command Example                    |
| ------- | ---------------------------- | ------------------------------------- |
| 55      | Check service status         | `systemctl status sshd`               |
| 56      | Start/stop/restart a service | `systemctl restart httpd`             |
| 57      | Enable/disable auto-start    | `systemctl enable nginx`              |
| 58      | List all running services    | `systemctl list-units --type=service` |
| 59      | Check service logs           | `journalctl -u httpd`                 |


🧱 9. Package Management
| 🔢 Task | 🧠 Objective                | 💻 Command Example  |
| ------- | --------------------------- | ------------------- |
| 60      | Install a package           | `dnf install httpd` |
| 61      | Remove a package            | `dnf remove httpd`  |
| 62      | List all installed packages | `rpm -qa`           |
| 63      | Check package info          | `dnf info nginx`    |
| 64      | Update all packages         | `dnf update -y`     |
| 65      | Clean repo cache            | `dnf clean all`     |



🕓 10. Scheduling and Automation
| 🔢 Task | 🧠 Objective              | 💻 Command Example       |
| ------- | ------------------------- | ------------------------ |
| 66      | Create a cron job         | `crontab -e`             |
| 67      | List existing cron jobs   | `crontab -l`             |
| 68      | Schedule a one-time task  | `at 10:30`               |
| 69      | Check cron service status | `systemctl status crond` |


🧾 11. Logs & Troubleshooting
| 🔢 Task | 🧠 Objective                | 💻 Command Example                |
| ------- | --------------------------- | --------------------------------- |
| 70      | Check system logs           | `cat /var/log/messages`           |
| 71      | View authentication logs    | `cat /var/log/secure`             |
| 72      | Search for “error” in logs  | `grep -i error /var/log/messages` |
| 73      | Monitor logs in real time   | `tail -f /var/log/syslog`         |
| 74      | Check failed login attempts | `grep "Failed" /var/log/secure`   |

🧩 12. System Boot / Shutdown
| 🔢 Task | 🧠 Objective              | 💻 Command Example |
| ------- | ------------------------- | ------------------ |
| 75      | Reboot system             | `reboot`           |
| 76      | Shutdown immediately      | `shutdown -h now`  |
| 77      | Schedule shutdown         | `shutdown -h +15`  |
| 78      | Cancel scheduled shutdown | `shutdown -c`      |
| 79      | Check last reboot time    | `who -b`           |


🔐 13. Security & Access
| 🔢 Task | 🧠 Objective                    | 💻 Command Example              |
| ------- | ------------------------------- | ------------------------------- |
| 80      | Edit sudo privileges            | `visudo`                        |
| 81      | Check sudo access               | `sudo -l`                       |
| 82      | List all active users           | `getent passwd`                 |
| 83      | Check failed SSH login attempts | `grep "Failed" /var/log/secure` |
| 84      | Change password policy          | Edit `/etc/login.defs`          |



🧮 14. Backup & Data Sync
| 🔢 Task | 🧠 Objective                | 💻 Command Example                     |
| ------- | --------------------------- | -------------------------------------- |
| 85      | Take directory backup       | `tar -cvf backup.tar /etc`             |
| 86      | Extract backup              | `tar -xvf backup.tar`                  |
| 87      | Sync files to remote server | `rsync -avz /data user@remote:/backup` |


🐚 15. Shell Scripting Basics
| 🔢 Task | 🧠 Objective                    | 💻 Command Example                  |
| ------- | ------------------------------- | ----------------------------------- |
| 88      | Write a hello-world script      | `echo "Hello Linux"`                |
| 89      | Write loop to print 1–5         | `for i in {1..5}; do echo $i; done` |
| 90      | Create a script to check uptime | `uptime >> /var/log/uptime.log`     |
| 91      | Schedule script via cron        | `crontab -e`                        |


🧠 Pro Tips for Interviews
✅ Practice on a VM (Rocky Linux / CentOS / Ubuntu)
✅ Know how to check service health & logs
✅ Be ready to troubleshoot network and disk issues
✅ Understand permissions, sudo, and cron well
✅ Keep examples ready for “what to do when system is slow / service down”


one of the most commonly asked and practical areas for L1/Linux Support Engineer interviews 👏

Boot-related issues test your ability to diagnose why a Linux system won’t start, recover access, and understand the boot sequence (BIOS → GRUB → Kernel → systemd).

⚙️ Linux Boot Related Issues & Tasks (For L0/L1 Engineer)
| Step | Stage           | What Happens                                       | Key Files / Commands                         |
| ---- | --------------- | -------------------------------------------------- | -------------------------------------------- |
| 1️⃣  | **BIOS / UEFI** | Hardware POST → finds bootable disk                | BIOS/UEFI settings                           |
| 2️⃣  | **MBR / GPT**   | Loads bootloader (GRUB)                            | `/boot` partition, MBR (first 512 bytes)     |
| 3️⃣  | **GRUB**        | Presents OS boot menu → loads kernel               | `/boot/grub2/grub.cfg`                       |
| 4️⃣  | **Kernel**      | Mounts root filesystem, starts `init` or `systemd` | `/boot/vmlinuz-*`, `/etc/fstab`              |
| 5️⃣  | **initramfs**   | Loads temporary drivers & modules                  | `/boot/initramfs-*`                          |
| 6️⃣  | **Systemd**     | Starts targets and services                        | `/lib/systemd/system`, `/etc/systemd/system` |
| 7️⃣  | **Login**       | Login prompt or GUI appears                        | `/etc/passwd`, `/etc/profile`                |


🔥 2. Common Boot-Related Issues
| Problem                                      | Root Cause                                 | Fix / Action                                            |
| -------------------------------------------- | ------------------------------------------ | ------------------------------------------------------- |
| 🔸 **GRUB prompt appears**                   | Missing/corrupt GRUB config                | Rebuild GRUB with rescue mode                           |
| 🔸 **Kernel panic: unable to mount root fs** | Wrong UUID in `/etc/fstab`, missing driver | Boot rescue → correct `/etc/fstab` or rebuild initramfs |
| 🔸 **initramfs prompt**                      | Disk, filesystem, or UUID issue            | `lsblk`, `blkid`, correct mounts, then `exit`           |
| 🔸 **System stuck at “Starting…”**           | Failed service or dependency               | Boot single-user mode → `journalctl -xb`                |
| 🔸 **Black screen after GRUB**               | Display manager/X issue                    | Boot in text mode → disable graphical.target            |
| 🔸 **Login prompt missing**                  | `getty` service issue                      | `systemctl start getty@tty1.service`                    |
| 🔸 **Boot partition full**                   | `/boot` out of space from old kernels      | Delete old kernels safely                               |
| 🔸 **Slow boot**                             | Failed mount or service timeout            | Check `systemd-analyze blame`                           |


🧠 3. Basic Boot Troubleshooting Commands
| Command                                  | Purpose                        |                           |
| ---------------------------------------- | ------------------------------ | ------------------------- |
| `journalctl -xb`                         | View detailed boot logs        |                           |
| `systemctl status`                       | Check running/failing services |                           |
| `dmesg                                   | less`                          | View kernel boot messages |
| `systemd-analyze`                        | Show total boot time           |                           |
| `systemd-analyze blame`                  | List slow services             |                           |
| `lsblk`, `blkid`, `cat /etc/fstab`       | Verify disk mounts             |                           |
| `df -h /boot`                            | Check space on boot partition  |                           |
| `grub2-mkconfig -o /boot/grub2/grub.cfg` | Rebuild GRUB configuration     |                           |
| `dracut -f`                              | Rebuild initramfs image        |                           |
| `grub2-install /dev/sda`                 | Reinstall GRUB bootloader      |                           |

🛠️ 4. Boot Recovery Tasks
| Task                                                | Description                          | Steps / Commands                                                                 |
| --------------------------------------------------- | ------------------------------------ | -------------------------------------------------------------------------------- |
| 🩹 **A. Boot into Rescue Mode**                     | Access minimal system to repair boot | - Boot from Linux ISO<br>- Choose *Troubleshooting → Rescue a system*            |
| 🧰 **B. Mount root filesystem**                     | Mount for chroot operations          | `chroot /mnt/sysimage`                                                           |
| 🔁 **C. Reinstall GRUB**                            | Fix bootloader                       | `bash grub2-install /dev/sda grub2-mkconfig -o /boot/grub2/grub.cfg `            |
| 🧱 **D. Rebuild Initramfs**                         | Fix missing modules/drivers          | `dracut -f /boot/initramfs-$(uname -r).img $(uname -r)`                          |
| 🧩 **E. Edit fstab**                                | Fix wrong UUID or mount paths        | `vi /etc/fstab` → correct UUIDs using `blkid`                                    |
| ⚙️ **F. Boot Single User Mode**                     | Boot to root shell for repair        | Edit GRUB → add `rd.break` or `single`                                           |
| 🗝️ **G. Reset Root Password (Interview favorite)** | Recover forgotten root password      | Boot with `rd.break` → remount `/sysroot` RW → `chroot /sysroot` → `passwd root` |
| 🧹 **H. Free Up Boot Space**                        | Delete old kernel images             | `dnf remove kernel-oldversion`                                                   |


🧾 5. Systemd Boot Targets
| Target              | Purpose                      | Command                                 |
| ------------------- | ---------------------------- | --------------------------------------- |
| `graphical.target`  | Multi-user + GUI             | `systemctl isolate graphical.target`    |
| `multi-user.target` | Multi-user text mode         | `systemctl isolate multi-user.target`   |
| `rescue.target`     | Single-user maintenance mode | `systemctl isolate rescue.target`       |
| `emergency.target`  | Minimal root shell           | `systemctl isolate emergency.target`    |
| `default.target`    | Default boot target          | `systemctl get-default` / `set-default` |


⚙️ 6. Practical Boot Troubleshooting Tasks
| 🔢 Task | Objective                               | Command / Procedure                       |           |
| ------- | --------------------------------------- | ----------------------------------------- | --------- |
| 1       | View boot logs                          | `journalctl -b`                           |           |
| 2       | Check services that failed to start     | `systemctl --failed`                      |           |
| 3       | Change default boot target to text mode | `systemctl set-default multi-user.target` |           |
| 4       | Change boot target back to GUI          | `systemctl set-default graphical.target`  |           |
| 5       | Boot into single-user mode for recovery | Edit GRUB → add `single` or `rescue`      |           |
| 6       | Rebuild GRUB configuration              | `grub2-mkconfig -o /boot/grub2/grub.cfg`  |           |
| 7       | Reinstall GRUB                          | `grub2-install /dev/sda`                  |           |
| 8       | Repair broken fstab entry               | Boot rescue → correct `/etc/fstab`        |           |
| 9       | Check which service delays boot         | `systemd-analyze blame`                   |           |
| 10      | View kernel logs for disk errors        | `dmesg                                    | grep sda` |
| 11      | Delete old kernel packages              | `dnf remove kernel-4.x.x`                 |           |
| 12      | Rebuild initramfs                       | `dracut -f`                               |           |


💣 7. Example Boot Issue Scenarios (Interview-style Q&A)
| Scenario                                        | Question               | Expected Action                                          |
| ----------------------------------------------- | ---------------------- | -------------------------------------------------------- |
| ❌ **Stuck at GRUB prompt**                      | How to recover system? | Boot from ISO → `chroot /mnt/sysimage` → reinstall GRUB  |
| ⚠️ **Kernel Panic – “unable to mount root fs”** | Likely cause?          | Wrong `/etc/fstab` or missing driver; rebuild initramfs  |
| ⚙️ **System boots to emergency mode**           | What to check?         | `/etc/fstab`, disk mounts, run `journalctl -xb`          |
| 🔒 **Forgot root password**                     | Recovery steps?        | Boot with `rd.break` → `chroot /sysroot` → `passwd root` |
| ⏱️ **System boots very slowly**                 | How to identify cause? | `systemd-analyze blame` → disable failing service        |
| 🧩 **Boot partition full**                      | How to fix?            | Remove old kernel images, clear `/boot`                  |


✅ 8. Preventive Best Practices

Keep 2–3 kernel versions only (clean old ones regularly).
Always use UUIDs instead of device names in /etc/fstab.
After kernel or GRUB updates → rebuild GRUB.
Maintain a bootable rescue ISO for emergencies.
Verify /boot partition size (minimum 1 GB recommended).
Document fstab entries & mounts.





































