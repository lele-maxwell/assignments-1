**1**: B
**2**:
Here are the difference between BIOS and UEFI
- The BIOS is an older version firmware in computers while the UEFI is a
  morden firmware in computers for booting
- The BIOS support older hardwarecomponents while the UEFI supports new and
  mordern devices
- The BIOS make use of the MBR for loading the OS while the UEFI make use
    of the EFI
-The BIOS being an older firmware for booting is more expese to insecurity
   as compared to thr UEFI which is of advace technology
-The UEFI supports drives of larger size as compared to the BIOS
**3**:
  command to list loaded modules
  *lsmod
  how to load a module
  ..use the command modprobe followed by the module name
  ..syntax: modprobe <module-name>
  ..for a module calles dummy the command id as follow
    modprobe dummy
  **4**:
  * /proc :This is a directory that contains information about system processes
    and hard ware .It holds settings and properties for the kernel
  * /sys: It is directory which contains system infos amd file system which provides
    provides the kernel properties,hardwares devices amd device drivers

    **SECTION 2**
    **5**
    * C:apt install package
    **6**
      Diffences between apt and dpkg
      * apt is an advance package manger while dpkg is an older pakage manager
      * apt is a high level as compared to dpkg which is a low-level package manager
      * apt is an advance tool pakage manager while dpkg isnot
      **7**:
      > command: apt purge ~o


      

       **8**:



      **SECTION 3**

      **9**:
      B:tail
      **10**:
      > cat /var/log/syslog | grep error | wc -l
      **11**:
      Diferrences between hard and soft link
      - hard links can't point accross different file system while a soft
        link can poing accoss different file system
      - hard links points to thesame inode as the original file while soft link
        points to different inode as the original file
      - hard links consumes less space as compared to soft links because of their
      - inode allocation on the disk storage
      - they are also different in syntax when creating
        ...hard link: ln <source-file> <link>
        ...soft link: ln -s <source-file> <link>
      **12**:
        > find /etc/*.conf -mtime 7 -daystart
      **13**:
        **Cron**:
        The cron daemon is abackground job that runs autamatically without
        forcefully the intervention human.it used in scheduling jobs to
        to tun after a particular period of time.This can be set  in the
        /etc/crontab configaration file which after save will persist over
        multiple reboot .
        **example**
         
         *  *  *  *  * user-name command to be executed
         *  12 25 12 * Maxwell date > backup.sh  
      
   * In the /ect/crontab file , the script above is entered
   * The script will siply print the date and time into the backup.sh file
   * **every day 25th , 12th month  at 12am every year**

  **14**:
  B:Disk usage in human-readable format
  **15**
  The UUID fiilesytem
   > cat /etc/fstab | cut -d ' ' -f 1 | grep UUID

  **16**:
  Comparing ext3 an ext4
  * ext3 file system is an older file system as compared to the ext4
  which is newer with more features the main differnce with ext3 and
  ext4 id the ext3 has a max size of a file is  2TB and max file system of 16TB
  while that of ext4 has a max size of a file is  16TB an a maxfile system
  of 8EB(exa-byte)
  Due to the differences in space of file system make the ext4 better than
  the ex2 .Other feature could be the journalng method of ext4 which
  ensure intergrity and hence enchances more security as compared to the
  ext3.

**17**:
You have added a new disk to the system and you want to create a new partition, 
format it with an ext4 filesystem, and mount it permanently at /data
the following steps can be folowed:
- Use the fdisk command lsblk to view all block devices including the
  device you want to partition (the name is noted)
- The partition command is used (sudo fdisk <path/device-name>)
  an interactive shell is opened where you could actually be used
  for partitioning
- Once in this shell the m(menue) button is pressed for more info
  Following the steps prompted in this shell will help partion the
  disk either primary,secondary or extended and an allocated size
  for the partition
- After the partition use the v key followed by w key to verify and
- write table and quite
- This partition can't be used for storing files or accssed unless it
   is being mounted with a file system
-Before that we create a directory called data (mountpoint directory)
usin the command
> mkdir /data
- use this command to mount in the mount point 
 mount -t <file-system>  <path/device-name>  <path/to/mount-point>/data
- To make it permanent, the command bellow could be use to ssave it in
 the /ect/fstab configuration file
> sudo echo " mount -t <file-system>  <path/device-name>  <path/to/mount-point>/data" >> /etc/fstab


**18**:
The /etc/fstab/ conguaration file is used to define hoe file systems 
(such as partition,network shares or removable devices) should be mounted
in the linux system.Changes here are permanent 
example
 mount -t <file-system>  <path/device-name>  <path/to/mount-point>/data

 **Bonus**:
 When the computer is turned on the system performs a POST (power on self test) and then the bootloader loads the kernal and initramfs from the  and the firmware loads the first stage of bootloader which the boot sector ( the first 512bits) and the second stage which loads the kernel the initramfs is used as a temporary filesystem which is used for the initialization of the kernel
 After these processes,the startup script is initialised

 
    
