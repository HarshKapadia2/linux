# Linux

## Table of Contents

-   [Introduction](#introduction)
-   [Endianness](#endianness)
-   [ELF](#elf)
-   [KVM and QEMU](#kvm-and-qemu)
-   [Shell Identification and Change](#shell-identification-and-change)
-   [Disks and Partitions](#disks-and-partitions)
    -   [Mounting, Partitioning and Formatting](#mounting-partitioning-and-formatting)
-   [AMD](#amd)
    -   [AMD History](#amd-history)
-   [Systemctl](#systemctl)
-   [PCIe](#pcie)
-   [SoC](#soc)
-   [Gathering System Information](#gathering-system-information)
-   [CPU Speed and CPU Clock](#cpu-speed-and-cpu-clock)
-   [NUMA](#numa)
-   [RAID](#raid)
-   [DMI](#dmi)
-   [Memory](#memory)
    -   [Memory Bandwidth](#memory-bandwidth)
    -   [DIMM](#dimm)
    -   [Memory Interleaving](#memory-interleaving)
-   [Niceness](#niceness)
-   [Context Switch](#context-switch)
-   [Protection Rings and Minix](#protection-rings-and-minix)
-   [Compatibility Software](#compatibility-software)
-   [Northbridge and Southbridge](#northbridge-and-southbridge)
-   [Interrupts and Exceptions](#interrupts-and-exceptions)
-   [ISA](#isa)
-   [X Server](#x-server)
-   [Desktop Environments](#desktop-environments)
-   [Locality of Reference](#locality-of-reference)
-   [Processing Hardware](#processing-hardware)
-   [Miscellaneous](#miscellaneous)

## Introduction

-   [The Missing Semester of Your CS Education](https://dev.harshkapadia.me/resources#the-missing-semester-of-cs-education)
-   [Putting the "You" in CPU](https://cpu.land/editions/one-pager)
-   [Modern Operating Systems by Andrew Tanenbaum (4th Edition)](files/books/tanenbaum-modern-operating-systems-4th-edition.pdf)
-   [Shell and Shell scripting](https://dev.harshkapadia.me/resources#shell-scripting)
-   [Read the Source Code of Shell Commands](https://www.baeldung.com/linux/read-source-code-shell-commands)
-   [What is POSIX? Why Does it Matter to Linux/UNIX Users?](https://itsfoss.com/posix)
-   [C programming](https://dev.harshkapadia.me/resources#c)
-   [Networking](https://networking.harshkapadia.me/linux)
-   [Operating System Boot Process](os-boot-process.md)
-   [Linux source code cross reference](https://elixir.bootlin.com/linux/v6.6.8/source)
-   [Latency numbers every programmer should know](https://gist.github.com/hellerbarde/2843375)
-   [Assembly](https://github.com/HarshKapadia2/assembly)

## Endianness

-   [Bit and Byte Ordering (Endianness)](bit-byte-ordering.md)

## ELF

-   ELF = Extensible and Linkable Format
-   [In-depth: ELF - The Extensible & Linkable Format](https://www.youtube.com/watch?v=nC1U1LJQL8o)

## KVM and QEMU

-   [Kernel-based Virtual Machine (KVM) and Quick Emulator (QEMU)](kvm-qemu.md)

## Shell Identification and Change

-   [Arrow keys, Home, End, tab-complete keys not working in shell](https://askubuntu.com/questions/325807/arrow-keys-home-end-tab-complete-keys-not-working-in-shell)
-   [How do I check which shell I am using?](https://askubuntu.com/questions/590899/how-do-i-check-which-shell-i-am-using)
    -   > $0 is the name of the running process. If you use it inside of a shell then it will return the name of the shell. If you use it inside of a script, it will be the name of the script.

## Disks and Partitions

-   [What Is `/dev/sda` in Linux?](https://www.baeldung.com/linux/dev-sda)
-   [How Is `/dev/vda` Different From `/dev/sda`?](https://www.baeldung.com/linux/vda-vs-sda)
-   [Understanding partition table with `sda1`, `sda2`, `sda5`](https://unix.stackexchange.com/questions/83781/understanding-partition-table-with-sda1-sda2-sda5)
-   [Difference between `sdX` and `vdX`](https://unix.stackexchange.com/questions/145332/difference-between-sdx-and-vdx)
-   [What is the difference between `/dev/sda` and `/dev/hda`?](https://unix.stackexchange.com/questions/175848/what-is-the-difference-between-dev-sda-and-dev-hda)
-   [Names for ATA and SATA disks in Linux](https://unix.stackexchange.com/questions/2447/names-for-ata-and-sata-disks-in-linux)
-   [How to list disks, partitions and filesystems in Linux?](https://unix.stackexchange.com/questions/157154/how-to-list-disks-partitions-and-filesystems-in-linux)

### Mounting, Partitioning and Formatting

-   [Mounting a device — role of /dev, /media and /mnt, and the mount command](https://unix.stackexchange.com/questions/13975/mounting-a-device-role-of-dev-media-and-mnt-and-the-mount-command)
-   [Correct way to mount a hard drive](https://unix.stackexchange.com/questions/72125/correct-way-to-mount-a-hard-drive)
-   [Mount Drives in Ubuntu Command Line](https://learnubuntu.com/mount-drives)
-   [Deleting All Partitions From the Command Line](https://serverfault.com/questions/250839/deleting-all-partitions-from-the-command-line)
-   [How to Format Disk Partitions in Linux](https://phoenixnap.com/kb/linux-format-disk)
-   [Quickest way to wipe an SSD clean of all its partitions for repartitioning in Linux?](https://superuser.com/questions/1284450/quickest-way-to-wipe-an-ssd-clean-of-all-its-partitions-for-repartitioning-in-li)

## AMD

-   AMD = Advanced Micro Devices
-   [Secrets of a $182 Billion Chip Maker: AMD's Labs](https://www.youtube.com/watch?v=7H4eg2jOvVw)
-   [AMD's CPU Analysis Lab Full Interview (Lasers, Scopes, & Silicon)](https://www.youtube.com/watch?v=hVSSOs9Z-uY)
-   [AMD's EPYC Rome Chips Crash After 1,044 Days of Uptime](https://www.tomshardware.com/news/amds-epyc-rome-chips-could-hang-after-1044-days-of-uptime)
-   [AMD CCD and CCX in Ryzen Processors Explained](https://www.hardwaretimes.com/amd-ccd-and-ccx-in-ryzen-processors-explained)
-   [How AMD Zen Almost Didn't Make It](https://www.youtube.com/watch?v=RTA3Ls-WAcw)
    -   [David Kaplan: When hardware must "just work"](https://www.youtube.com/watch?v=e2vPp0fQUkM)

### AMD History

-   [AMD: How It All Began](https://www.youtube.com/watch?v=mb53IYjZlNc)
-   [Intel & AMD: The First 30 Years](https://www.youtube.com/watch?v=kZ9ntfjytTI)
-   [AMD: The Incredible Adventure Continues](https://www.youtube.com/watch?v=TbWfywgY7sk)
-   [How AMD Left GlobalFoundries for TSMC](https://www.youtube.com/watch?v=oAlU6vQ1Pn8)

## Systemctl

-   [Systemctl vs Systemd](https://www.reddit.com/r/redhat/comments/qefrhm/systemctl_vs_systemd_vs_service)
-   [What is Systemctl? An In-Depth Overview](https://www.liquidweb.com/kb/what-is-systemctl-an-in-depth-overview)

## PCIe

-   PCIe = Peripheral Component Interconnect Express
-   Used to connect hardware devices like graphics cards, NICs, sound cards, capture cards, etc to the motherboard.
-   [PCI Express (PCIe) 3.0](https://www.youtube.com/watch?v=LSSHuMHbCWo)
-   [Explaining PCIe Slots](https://www.youtube.com/watch?v=PrXwe21biJo)
-   [Understanding M.2, SATA, PCIe and NVMe SSDs](https://www.crucial.com/articles/about-ssd/m2-with-pcie-or-sata)
-   [SATA vs SAS vs PCIe](https://www.youtube.com/watch?v=JJi-NGZeyxA)

## SoC

-   SoC = System on Chip
-   [What is a System on Chip (SoC)?](https://anysilicon.com/what-is-a-system-on-chip-soc)
-   [What is the difference between a motherboard and an SOC?](https://www.quora.com/What-is-the-difference-between-a-motherboard-and-an-SOC)
    -   [Motherboards Explained](https://www.youtube.com/watch?v=BBAvz6jZEik)

## Gathering System Information

-   [cli.harshkapadia.me/terminal#gathering-system-information](https://cli.harshkapadia.me/terminal#gathering-system-information)

## CPU Speed and CPU Clock

-   [What is Processor Speed and Why Does It Matter?](https://www.hp.com/us-en/shop/tech-takes/what-is-processor-speed)
-   [What Is Clock Speed?](https://www.intel.com/content/www/us/en/gaming/resources/cpu-clock-speed.html)
-   [Intructions vs cycles per second - what is actually measured in Hertz?](https://stackoverflow.com/questions/62577798/intructions-vs-cycles-per-second-what-is-actually-measured-in-hertz)
-   [Difference between clock cycle, machine cycle and instruction cycle of the CPU](https://electronics.stackexchange.com/questions/529562/difference-between-clock-cycle-machine-cycle-and-instruction-cycle-of-the-cpu)
-   [What is a clock cycle and clock speed?](https://stackoverflow.com/questions/43651954/what-is-a-clock-cycle-and-clock-speed)
-   [Why do we need a CPU clock](https://superuser.com/questions/1021499/why-do-we-need-a-cpu-clock)
-   [Inside a CPU, what happens in a single clock cycle?](https://electronics.stackexchange.com/questions/373417/inside-a-cpu-what-happens-in-a-single-clock-cycle)

## NUMA

-   NUMA = Non-Uniform Memory Access
-   [What is NUMA?](https://www.techtarget.com/whatis/definition/NUMA-non-uniform-memory-access)
-   [NUMA (Wikipedia)](https://en.wikipedia.org/wiki/Non-uniform_memory_access)

## RAID

-   RAID = Redundant Array of Independent Disks
-   [What is RAID Storage? Meaning, Types, and Working](https://www.spiceworks.com/tech/data-management/articles/what-is-raid-storage)
-   [Should I use Raid 6 or Raid Z2? What are the advantages/disadvantages of each?](https://www.reddit.com/r/homelab/comments/6lisv9/should_i_use_raid_6_or_raid_z2_what_are_the)
-   [RAIDZ Levels](https://raidz-calculator.com/raidz-types-reference.aspx)
-   [ZFS 101—Understanding ZFS storage and performance](https://arstechnica.com/information-technology/2020/05/zfs-101-understanding-zfs-storage-and-performance)
-   [ZFS RAIDZ vs. traditional RAID](https://www.klennet.com/notes/2019-07-04-raid5-vs-raidz.aspx)
-   [Linux RAID vs ZFS RAID](https://www.45drives.com/community/articles/linux-raid-vs-zfs-raid)
-   [Configuring ZFS on Ubuntu 20.04](https://linuxconfig.org/configuring-zfs-on-ubuntu-20-04)

## DMI

-   DMI = Desktop Management Information
-   Access this data using the command `dmidecode`.
-   [What is DMI?](https://www.linuxquestions.org/questions/linux-newbie-8/what-is-dmi-445952)
-   [DMI vs SMBIOS](https://en.wikipedia.org/wiki/Desktop_Management_Interface#DMI_and_SMBIOS)
    -   [Does UEFI replace standards like SMBIOS and ACPI?](https://stackoverflow.com/questions/66603762/does-uefi-replace-standards-like-smbios-and-acpi)

## Memory

-   [Memory refresh](https://en.wikipedia.org/wiki/Memory_refresh)
-   [Why aren't SSDs as fast as RAM?](https://www.reddit.com/r/pcmasterrace/comments/g6xgq9/comment/fodrvce)
-   [Why we don't use RAM drive as the Hard Drive Disk?](https://superuser.com/questions/1357655/why-we-dont-use-ram-drive-as-the-hard-drive-disk)

### Memory Bandwidth

-   [Memory Bandwidth (Wikipedia)](https://en.wikipedia.org/wiki/Memory_bandwidth)
-   [Computer Memory Speed and Latency](https://www.lifewire.com/pc-memory-speed-and-latency-832450)
-   [The Complete Guide to RAM Speeds](https://whatintech.com/ddr4-2400-vs-2666-vs-3000-vs-3200-vs-3600-vs-4000-mhz)

### DIMM

-   DIMM = Dual In-line Memory Module
-   [What Is a Dual In-line Memory Module (DIMM)? Meaning, Characteristics, and Types](https://www.spiceworks.com/tech/tech-general/articles/what-is-dimm)
-   [Single Rank vs Dual Rank RAM: Differences & Performance Impact](https://www.cgdirector.com/single-rank-vs-dual-rank-ram)

### Memory Interleaving

-   [Interleaved memory](https://en.wikipedia.org/wiki/Interleaved_memory)
-   [What is Memory Interleaving? & Advantages](https://datatrained.com/post/memory-interleaving)

## Niceness

-   [how greedy are your processes?](https://www.youtube.com/watch?v=GsF8R6DBxSg)
-   [Difference between nice value and priority in the top output](https://superuser.com/questions/203657/difference-between-nice-value-and-priority-in-the-top-output/877353#877353)

## Context Switch

-   [Context Switching in OS](https://www.baeldung.com/cs/os-cpu-context-switch)
-   [Scheduler vs Dispatcher](https://stackoverflow.com/questions/27421239/what-is-the-difference-between-scheduler-and-dispatcher-in-context-of-process-sc)

## Protection Rings and Minix

-   Anil Harwani told us about [the Tanenbaum-Torvalds debate](https://en.wikipedia.org/wiki/Tanenbaum%E2%80%93Torvalds_debate) on [OTC CatchUp #145](https://catchup.ourtech.community/summary/145), which was an argument where Tanenbaum was trying to prove why a Microkernel architecture (Tanenbaum's OS Minix had that architecture.) is better than a Monolithic Kernel architecture that Torvald's Linux has.
    -   Kernel architectures
        -   [Microkernel vs Monolithic Kernel](https://stackoverflow.com/questions/4537850/what-is-difference-between-monolithic-and-micro-kernel)
        -   [Difference between Microkernel and Monolithic Kernel](https://www.geeksforgeeks.org/difference-between-microkernel-and-monolithic-kernel)
    -   Minix
        -   Tanenbaum initially created the [Minix](https://en.wikipedia.org/wiki/Minix) Operating System for educational purposes.
        -   Anil also told us how Minix was found inside the [Intel Management Engine](https://en.wikipedia.org/wiki/Intel_Management_Engine), which was a big deal, as Minix, whose goal was never to have military-grade security, was being used on billions of machines at a privilege level that is higher than the kernel, and that made billions of machines vulnerable. Also, this implies that Minix is the most used OS on the planet.
            -   [Replace Your Exploit-Ridden Firmware with Linux](https://www.youtube.com/watch?v=iffTJ1vPCSo)
                -   The first 12 minutes of this video is sufficient to understand how vulnerable systems are.
                -   [Protection Rings (-3, -2, -1, 0, 1, 2, 3)](https://security.stackexchange.com/questions/129098/what-is-protection-ring-1)
            -   [MINIX: Intel's hidden in-chip operating system](https://www.zdnet.com/article/minix-intels-hidden-in-chip-operating-system)
            -   [What is MINIX? The most popular OS in the world, thanks to Intel](https://www.networkworld.com/article/3236064/minix-the-most-popular-os-in-the-world-thanks-to-intel.html)
            -   Tanenbaum also wrote [An Open Letter to Intel](https://www.cs.vu.nl/~ast/intel).
        -   [USBAnywhere and the History of Baseboard Management Controllers (BMCs)](https://www.youtube.com/watch?v=5PcsLSW32Rc)

## Compatibility Software

-   [Cygwin vs MinGW vs MSys/Msys2 vs WSL](https://www.sobyte.net/post/2021-11/cygwin-mingw-msys)

## Northbridge and Southbridge

-   [What are the north and south bridges of a motherboard?](https://superuser.com/questions/1152648/what-are-the-north-and-south-bridges-of-a-motherboard)
-   [Chipsets Explained – Northbridge and Southbridge](https://www.skillsbuildtraining.com/chipsets-explained-northbridge-and-southbridge)

## Interrupts and Exceptions

-   [Interrupts vs Exceptions (Faults, Traps and Aborts)](https://stackoverflow.com/questions/3149175/what-is-the-difference-between-trap-and-interrupt)
-   [External Interrupts in the x86 system: Interrupt controller evolution](https://habr.com/en/articles/446312) (PIC, PIR, APIC, LAPIC, MSI, etc.)

## ISA

-   ISA = Instruction Set Architecture
-   [Instruction Set Architectures](isa.md)

## X Server

-   [What is the X server?](https://askubuntu.com/questions/7881/what-is-the-x-server)
-   [What are X server, display and screen?](https://unix.stackexchange.com/questions/503806/what-are-x-server-display-and-screen)
-   [X Window authorization](https://en.wikipedia.org/wiki/X_Window_authorization)

## Desktop Environments

-   [What is KDE, GTK, GTK+, QT, and/or GNOME?](https://askubuntu.com/questions/249150/what-is-kde-gtk-gtk-qt-and-or-gnome)
    -   [Full form of KDE](https://fullforms.com/KDE)
    -   [Full form of Qt](https://stackoverflow.com/questions/22361655/what-does-qt-stand-for)
    -   GNOME: GNU Network Object Model Environment
-   [KDE Vs GNOME Vs Xfce; Which is the Best Desktop Environment and Why?](https://cloudzy.com/blog/kde-vs-gnome-vs-xfce)
-   [GNOME vs Xfce vs KDE](https://www.vpsserver.com/gnome-vs-xfce-vs-kde)
-   [Is there a breakdown of the differences between GNOME, KDE, and Xfce desktop environments?](https://superuser.com/questions/88249/is-there-a-breakdown-of-the-differences-between-gnome-kde-and-xfce-desktop-env)
-   [What is gdm3, kdm, lightdm? How to install and remove them?](https://askubuntu.com/questions/829108/what-is-gdm3-kdm-lightdm-how-to-install-and-remove-them)

## Locality of Reference

-   [Locality of reference](https://en.wikipedia.org/wiki/Locality_of_reference)
    -   Mainly Temporal and Spatial Locality
-   [Non-Temporal Data](https://www.nic.uoregon.edu/~khuck/ts/acumem-report/manual_html/ch05s03.html)

## Processing Hardware

-   [CPU vs GPU vs TPU vs DPU vs QPU](https://www.youtube.com/watch?v=r5NQecwZs1A)
-   [CPU, GPU.....DPU?](https://www.youtube.com/watch?v=pQrM5L6C-FQ)
-   [CPU vs GPU (What's the Difference?)](https://www.youtube.com/watch?v=_cyVDoyI6NE)
-   [What's the Difference Between an APU, CPU, and GPU?](https://www.makeuseof.com/tag/what-is-the-difference-between-an-apu-a-cpu-and-a-gpu-makeuseof-explains)
-   [FPGA vs CPU vs GPU vs Microcontroller: How Do They Fit into the Processing Jigsaw Puzzle?](https://www.arrow.com/en/research-and-events/articles/fpga-vs-cpu-vs-gpu-vs-microcontroller)
-   [What is an NPU? Here’s why everyone’s suddenly talking about them](https://www.digitaltrends.com/computing/what-is-npu)
-   [AI 101: GPU vs. TPU vs. NPU (+ ASICs vs FPGAs)](https://www.backblaze.com/blog/ai-101-gpu-vs-tpu-vs-npu)

## Miscellaneous

-   Computerraria: [I Made a 32-bit Computer Inside Terraria](https://www.youtube.com/watch?v=zXPiqk0-zDY)
-   [Ubuntu Desktop vs Ubuntu Server](https://www.makeuseof.com/tag/difference-ubuntu-desktop-ubuntu-server)
-   [User vs group](https://askubuntu.com/questions/740725/what-is-difference-between-group-and-user)
-   [OEM vs ODM vs OBM](https://www.scadatw.com/odm)
-   ["Reboot Even If System Utterly Broken"](http://www.alexander-miles.com/?p=200)
-   [MiB vs MB](https://digilent.com/blog/mib-vs-mb-whats-the-difference)
