# Linux Basics

🐧 **What is Linux?**

Linux is an operating system (OS) — just like Windows or macOS. An operating system lets you use your computer by:
1. Managing files
2. Running programs
3. Connecting hardware (keyboard, mouse, etc.) with software (apps)

What makes Linux special:
- It’s free — you don’t have to pay to use it.
- It’s open-source — anyone can see how it’s made, change it, or improve it.
- It’s secure and stable — it almost never crashes or gets viruses.
- It’s used everywhere — from phones (Android is based on Linux!) to supercomputers, servers, and even space rockets.

## Quick comparison

| Feature                    | Linux                        | Windows                   | macOS                           |
| -------------------------- | ---------------------------- | ------------------------- | ------------------------------- |
| 💸 Cost                    | Free                         | Paid                      | Paid (comes with Apple devices) |
| 🔒 Security                | Very secure                  | Often targeted by viruses | Quite secure                    |
| ⚙️ Customization           | Fully customizable           | Limited                   | Limited                         |
| 💻 Speed & Performance     | Fast, even on old computers  | Can be slow on old PCs    | Smooth on Apple hardware        |
| 🔧 Control                 | Full control over everything | Restricted                | Restricted                      |
| 🧠 Learning curve          | A bit harder at first        | Easy                      | Easy                            |

## Why people use Linux

- Developers love it for coding.  
- Servers use it because it’s reliable and rarely “just crashes.”  
- Privacy lovers use it because it doesn’t spy on you.  
- Tinkerers love customizing everything — from the desktop look to the system itself.

## Examples of Linux versions (distributions)

There are two big “families” of Linux distributions:

- 🟥 RPM-based (Red Hat family): CentOS, RHEL, Rocky Linux  
- 🟩 DEB-based (Debian family): Ubuntu

They’re both Linux — just different ways of managing software and organizing the system.

### What does “RPM-based” mean?

RPM stands for Red Hat Package Manager. It’s a system Linux uses to install, update, and remove software packages (files ending in `.rpm`). An RPM-based Linux distribution uses the RPM format for its software packages and is often related to Red Hat Linux in some way.

## Popular RPM-based Linux Distributions

### 1. Red Hat Family (Enterprise & Professional)

| Distribution                        | Description                                                          |
| ----------------------------------- | -------------------------------------------------------------------- |
| **RHEL (Red Hat Enterprise Linux)** | Commercial, stable, used by companies and servers.                   |
| **CentOS Stream**                   | Free version of RHEL that shows what’s coming next in Red Hat.       |
| **Oracle Linux**                    | RHEL-compatible, maintained by Oracle; often used on servers.        |
| **Rocky Linux**                     | Community-driven replacement for CentOS, fully compatible with RHEL. |
| **AlmaLinux**                       | Another free RHEL-compatible distro; stable and enterprise-grade.    |

### 2. Fedora Family (Cutting Edge / Developer-Focused)

| Distribution           | Description                                                       |
| ---------------------- | ----------------------------------------------------------------- |
| **Fedora Workstation** | Great for developers and desktop users; upstream source for RHEL. |
| **Fedora Server**      | Server version of Fedora.                                         |
| **Fedora Silverblue**  | Immutable desktop system (safer, harder to break).                |

### 3. Other RPM-based Distros

| Distribution            | Description                                                               |
| ----------------------- | ------------------------------------------------------------------------- |
| **openSUSE Leap**       | Stable, enterprise-grade; uses RPM with its own management tool (zypper). |
| **openSUSE Tumbleweed** | Rolling-release version (always up-to-date).                              |
| **Mageia**              | Community continuation of Mandriva Linux.                                 |
| **ROSA Linux**          | Russian fork of Mandriva, desktop-friendly.                               |
| **PCLinuxOS**           | User-friendly, rolling-release RPM distro.                                |
| **ALT Linux**           | Another Russian Linux distro derived from Mandriva.                       |

## Summary

| Family             | Example Distros                          | Type              |
| ------------------ | ---------------------------------------- | ----------------- |
| **Red Hat-based**  | RHEL, CentOS Stream, Rocky, Alma, Oracle | Enterprise        |
| **Fedora-based**   | Fedora Workstation, Silverblue           | Desktop/Developer |
| **openSUSE-based** | openSUSE Leap, Tumbleweed                | Desktop/Server    |
| **Mandriva-based** | Mageia, ROSA, PCLinuxOS                  | Desktop           |

## RPM-based vs DEB-based Linux

| Feature                        | 🟥 RPM-based                                                   | 🟩 DEB-based                                               |
| ------------------------------ | -------------------------------------------------------------- | ---------------------------------------------------------- |
| 💿 Package Format               | `.rpm` (Red Hat Package Manager)                               | `.deb` (Debian Package)                                    |
| 🧰 Common Package Managers      | `dnf`, `yum`, or `zypper`                                      | `apt`, `dpkg`, or `apt-get`                                |
| 🌳 Main Families                | Red Hat → Fedora, CentOS Stream, Rocky, Alma, openSUSE         | Debian → Ubuntu, Linux Mint, MX Linux                      |
| 🏢 Main Focus                   | Enterprise servers, stability, professional environments       | Desktop use, community friendliness, simplicity            |
| ⚙️ System Management            | Uses **systemd** and **dnf** for updates; RHEL-style config    | Uses **systemd** and **apt**; simpler commands             |
| 🧩 Software Availability        | Huge repositories, but sometimes slower to get latest desktop apps | Massive repositories, often more desktop apps & faster updates |
| 💼 Commercial Support           | Strong (Red Hat, SUSE, Oracle)                                 | Mostly community, some Ubuntu enterprise support           |
| 🧠 Learning Curve               | Slightly steeper; more manual control                          | Easier for beginners; more guides online                   |
| 🧾 Examples                     | Fedora, RHEL, CentOS Stream, Rocky, AlmaLinux, openSUSE        | Ubuntu, Debian, Linux Mint, Pop!_OS, Zorin OS              |

## Summary in Simple Words

- 🟥 RPM-based distros (like Fedora, RHEL, openSUSE): great for servers, developers, and professionals who want reliability and control.  
- 🟩 DEB-based distros (like Ubuntu, Linux Mint, Debian): best for beginners and desktop users — easier to install software and get help online.

## Quick Example

Install Firefox:

On RPM-based systems:
```sh
sudo dnf install firefox
```

On DEB-based systems:
```sh
sudo apt install firefox
```

---

## Linux Family Tree (Simplified)

```
                 🐧 LINUX KERNEL
                       │
        ┌──────────────┴────────────────┐
        │                               │
   🟥 RPM-based (Red Hat Family)     🟩 DEB-based (Debian Family)
        │                               │
        │                               │
   ┌────┴─────┐                     ┌───┴──────┐
   │          │                     │          │
Red Hat    openSUSE              Debian     Ubuntu
 Enterprise   │                     │          │
   │          │                     │          │
   │       ┌──┴───┐             ┌───┴───┐  ┌───┴────┐
   │       │      │             │       │  │        │
 Fedora  SUSE   Mageia        MX Linux  Kali     Linux Mint
   │                      (lightweight) (security)  │
   │                                               │
 CentOS Stream, Rocky, AlmaLinux                Zorin OS, Pop!_OS
```

### What this shows

The Linux kernel is the base — every distribution builds on it. Two main “families”:

- 🟥 RPM-based → Focused on enterprise and stability (Red Hat, Fedora, openSUSE)
- 🟩 DEB-based → Focused on ease of use and desktops (Debian, Ubuntu, Mint)

From there, many child distributions branch out and specialize:
- Fedora → RHEL, Rocky, AlmaLinux (servers)
- Ubuntu → Mint, Pop!_OS, Zorin OS (desktops)

Common notes:
- Ubuntu — easiest for beginners  
- Linux Mint — looks like Windows  
- Fedora — modern and fast  
- Debian — stable and trusted  
- Arch Linux — for power users

=====================================================================================
