# Linux L0 / L1 Admin Tasks — Quick Reference & Interview Guide

A concise, practical guide for Linux L0/L1 (Support) engineers covering the most commonly used commands, daily support tasks, troubleshooting techniques, and boot recovery procedures. This README converts the raw checklist into an easy-to-read learning resource you can use to prepare for interviews or day-to-day support work.

Table of contents
- About
- How to use this guide
- Quick reference: essential commands (by topic)
- Practical tasks (top interview-focused tasks)
- Boot & recovery: sequence, common issues and fixes
- Interview-style scenarios and suggested actions
- Short study checklist (L0/L1)
- Best practices & preventive measures
- Contributing / Notes / License

---

About
-----
This guide is designed to give you fast, actionable commands and approaches for everyday Linux support tasks and common interview questions. It assumes a basic UNIX/Linux familiarity and focuses on tools and commands you will use frequently.

How to use this guide
---------------------
- Read the Quick Reference to become comfortable with common commands.
- Practice the Practical Tasks on a VM (e.g., Ubuntu, Rocky/CentOS).
- Use Boot & Recovery when preparing for troubleshooting or incident response.
- Memorize the Short Study Checklist for interview readiness.

Quick reference: essential commands (by topic)
----------------------------------------------

System Navigation & File Management
- Show current directory:
  ```bash
  pwd
  ```
- List files:
  ```bash
  ls -l          # long listing
  ls -a          # include hidden
  ls -lh         # human readable sizes
  ```
- Change directories:
  ```bash
  cd /path
  cd ..          # parent
  cd /           # root
  ```
- Create, view and edit:
  ```bash
  mkdir dir
  rmdir dir
  touch file
  cat file
  less file
  more file
  vi file        # or nano
  cp file dest
  mv file dest
  rm file
  ```
- Searching:
  ```bash
  find / -name filename
  locate filename
  file filename   # determine file type
  head file
  tail file
  tail -f logfile
  ```

File Permissions & Ownership
- Change permissions and ownership:
  ```bash
  chmod 755 file
  chown user:group file
  umask           # show or set default permissions
  ls -ld dirname
  namei -l /path/to/file   # check effective permission along path
  ```

User & Group Management
- Manage users and groups:
  ```bash
  useradd username   # or adduser
  passwd username
  usermod -aG group username
  groupadd groupname
  id username
  whoami
  who
  w
  su - user
  sudo command
  ```
- Sudoers and privileges:
  ```bash
  visudo
  sudo -l
  ```

Process & System Monitoring
- View and manage processes:
  ```bash
  ps -ef
  top               # or htop
  pgrep processname
  kill -9 PID
  pkill processname
  nice, renice
  ```
- System metrics:
  ```bash
  free -m
  uptime
  vmstat
  iostat
  sar
  ```

Disk, Filesystem & Storage
- Disk usage and devices:
  ```bash
  df -h
  du -sh *
  lsblk
  fdisk -l
  parted -l
  mount /dev/sdb1 /mnt
  umount /mnt
  blkid
  cat /etc/fstab
  ```
- Swap:
  ```bash
  swapon -s
  swapon /dev/sdbX
  swapoff /dev/sdbX
  mkswap /dev/sdbX
  ```

Networking & Connectivity
- Interfaces and routing:
  ```bash
  ip a
  ifconfig      # older systems
  ip route
  hostnamectl
  ```
- Diagnostics:
  ```bash
  ping 8.8.8.8
  traceroute host
  mtr host
  ss -tulnp
  netstat -tulnp   # older systems
  nslookup host
  dig host
  curl URL
  wget URL
  scp file user@host:/path
  sftp user@host
  ssh user@host
  ```

System Services & Startup (systemd)
- Manage services:
  ```bash
  systemctl status servicename
  systemctl start|stop|restart servicename
  systemctl enable|disable servicename
  systemctl --failed
  systemctl list-units --type=service
  journalctl -u servicename
  ```
- Legacy service tools for older distros:
  ```bash
  service servicename status
  chkconfig
  update-rc.d
  ```

Logs & Troubleshooting
- Common log locations:
  - Systemd: journalctl
  - RHEL/CentOS: /var/log/messages, /var/log/secure
  - Debian/Ubuntu: /var/log/syslog
- Useful commands:
  ```bash
  journalctl -xe
  journalctl -b
  journalctl -u servicename
  dmesg | less
  grep -i error /var/log/messages
  tail -f /var/log/syslog
  ```
- Text tools:
  ```bash
  grep, awk, sed, cut, sort, uniq, wc
  ```

Package Management
- RHEL/CentOS/Rocky:
  ```bash
  dnf install pkg
  dnf update -y
  rpm -qa
  dnf remove pkg
  ```
- Debian/Ubuntu:
  ```bash
  apt update
  apt install pkg
  apt-get upgrade
  dpkg -l
  ```

Compression & Archiving
- Tar, gzip, zip:
  ```bash
  tar -czvf backup.tar.gz /dir
  tar -xvf archive.tar.gz
  gzip file
  gunzip file.gz
  zip -r archive.zip folder
  unzip archive.zip
  rsync -avz /src /dest
  ```

Shell & Scripting Basics
- Shebang and basics:
  ```bash
  #!/bin/bash

  echo "Hello Linux"
  for i in {1..5}; do echo $i; done
  if [ -f /etc/passwd ]; then echo "exists"; fi
  read -p "Enter name: " name
  ```
- Scheduling:
  ```bash
  crontab -e
  crontab -l
  at 10:30
  systemctl list-timers
  ```

System Information & Hardware
- Commands:
  ```bash
  uname -a
  cat /etc/os-release
  lscpu
  lsusb
  lspci
  dmidecode
  who -b
  ```

Practical tasks (Top 10 / interview-focused)
---------------------------------------------
These are the tasks you should be able to perform quickly during interviews or day-to-day.

1. Check system uptime, CPU and memory:
   ```bash
   uptime
   top
   free -m
   ```
2. Restart a failed service:
   ```bash
   systemctl restart httpd
   systemctl status httpd
   ```
3. Find large files using disk:
   ```bash
   du -ahx / | sort -rh | head -20
   find / -type f -size +500M
   ```
4. Monitor logs for errors:
   ```bash
   tail -f /var/log/messages
   grep -i error /var/log/messages
   ```
5. Check which ports are open:
   ```bash
   ss -tulnp
   ```
6. Add a user and grant sudo:
   ```bash
   useradd user1
   passwd user1
   usermod -aG wheel user1   # RHEL/CentOS
   usermod -aG sudo user1    # Ubuntu/Debian
   ```
7. Test network connectivity:
   ```bash
   ping 8.8.8.8
   curl -I https://example.com
   nslookup google.com
   ```
8. Schedule a cron job:
   ```bash
   crontab -e
   # add: 0 2 * * * /usr/local/bin/backup.sh
   ```
9. Mount an extra disk:
   ```bash
   lsblk
   mount /dev/sdb1 /mnt
   ```
10. Find high CPU process:
    ```bash
    ps -eo pid,comm,%cpu,%mem --sort=-%cpu | head
    ```

Boot & recovery: sequence, common issues and fixes
--------------------------------------------------
Boot sequence in brief:
1. BIOS / UEFI → finds bootable disk
2. MBR / GPT → load bootloader (GRUB)
3. GRUB → select kernel & initramfs
4. Kernel → mounts root filesystem and starts init/systemd
5. initramfs → loads temporary drivers
6. systemd → brings up services and targets
7. Login prompt or GUI

Common boot problems and quick actions
- GRUB prompt appears: missing/corrupt GRUB config.
  - Boot from rescue ISO, chroot, reinstall GRUB.
- Kernel panic "unable to mount root fs": wrong UUID or missing driver.
  - Boot rescue, check /etc/fstab and blkid, rebuild initramfs.
- initramfs prompt: disk or UUID mismatch.
  - Use lsblk, blkid, correct /etc/fstab, then reboot.
- System stuck at “Starting …”: failing service.
  - Boot single-user or rescue mode, check journalctl -xb.
- Boot partition full: remove old kernels safely.
  - Use package manager to remove old kernel packages.

Useful boot commands
```bash
journalctl -xb
systemctl --failed
dmesg | less
systemd-analyze
systemd-analyze blame
lsblk
blkid
cat /etc/fstab
df -h /boot
grub2-mkconfig -o /boot/grub2/grub.cfg   # RHEL/CentOS
dracut -f                                 # rebuild initramfs
grub2-install /dev/sda
```

Boot recovery checklist (high level)
1. Boot from a rescue ISO if system won't start normally.
2. Mount root filesystem (usually under /mnt/sysimage).
3. chroot /mnt/sysimage to make repairs.
4. Fix /etc/fstab, rebuild initramfs, reinstall GRUB as needed.
5. Check logs (journalctl -xb) and /var/log for errors.
6. Reboot and verify.

Example rescue commands (RHEL/CentOS style)
```bash
# from rescue environment
lsblk
mount /dev/mapper/centos-root /mnt/sysimage
mount --bind /dev /mnt/sysimage/dev
mount --bind /proc /mnt/sysimage/proc
mount --bind /sys /mnt/sysimage/sys
chroot /mnt/sysimage
grub2-install /dev/sda
grub2-mkconfig -o /boot/grub2/grub.cfg
dracut -f
exit
reboot
```

Interview-style scenarios and suggested actions
----------------------------------------------
- Stuck at GRUB prompt: Boot from live ISO → chroot → reinstall GRUB.
- Kernel panic "unable to mount root fs": Verify /etc/fstab UUIDs vs blkid, correct and rebuild initramfs.
- Boots to emergency mode: Run journalctl -xb, check /etc/fstab and disk health.
- Forgot root password: Boot with rd.break or emergency, remount sysroot as rw, chroot and passwd root (depends on distro/UEFI/SecureBoot).
- Slow boot: systemd-analyze blame → disable/inspect slow services.

Short study checklist (L0/L1)
-----------------------------
- Boot process (GRUB → init/systemd)
- systemctl basics and journaling (journalctl)
- User management & sudoers
- File permissions and special bits (sticky, SUID, SGID)
- Disk usage and mount troubleshooting
- Network troubleshooting (ping, ss, dig)
- Basic scripting + cron
- How to recover when a service fails / system becomes unresponsive

Best practices & preventive measures
-----------------------------------
- Keep 2–3 kernel versions only; remove old kernels periodically.
- Use UUIDs in /etc/fstab instead of /dev/sdXY device names.
- Keep a bootable rescue ISO and documented recovery steps.
- Monitor /boot space and disk usage (alerting).
- Test backups and document fstab & mount points.
- After kernel/GRUB updates, verify and rebuild GRUB if necessary.

Contributing / Notes
--------------------
- This guide is a practical quick reference — not a replacement for full manuals.
- Practice commands in a lab/VM before running on production systems.
- If you want improvements, open a PR or create issues on the repository.

License
-------
This is provided as-is for study and interview preparation. No warranty. Use responsibly.

--- 

Happy learning — practice regularly on a VM and keep this README as a pocket guide during interviews and on-call shifts.