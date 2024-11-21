### **Solutions**

---

#### **Section 1: System Architecture**

1. **Answer**:  
   **B. `lscpu`**  
   The `lscpu` command provides detailed information about the CPU architecture.

2. **Answer**:  
   **BIOS vs UEFI**:  
   - **BIOS**: Uses a 16-bit mode, limited to 1MB addressable space. Bootloader starts in MBR format, which supports disks up to 2TB.  
   - **UEFI**: Supports 64-bit mode, larger disk sizes, and GPT partitioning. UEFI includes secure boot and faster boot times compared to BIOS.

3. **Answer**:  
   **Command**:  
   ```
   lsmod  # Displays loaded kernel modules
   sudo modprobe dummy  # Loads the 'dummy' kernel module
   ```

4. **Answer**:  
   - **/proc**: A virtual filesystem containing runtime system information like process and memory. For example, `/proc/cpuinfo` for CPU details.  
   - **/sys**: Provides an interface to kernel objects. It is used to query and manage hardware settings.

---

#### **Section 2: Linux Installation and Package Management**

5. **Answer**:  
   **C. `apt install package`**  
   The `apt` command is the standard tool for package installation on Debian-based systems.

6. **Answer**:  
   - **apt**: High-level tool that resolves dependencies and interacts with repositories.  
   - **dpkg**: Low-level tool for installing `.deb` files. Does not handle dependencies.

7. **Answer**:  
   **Command**:  
   ```
   sudo apt autoremove
   ```

8. **Answer**:  
   **Steps**:  
   Create a file `/etc/yum.repos.d/example.repo` with the following content:  
   ```
   [example-repo]
   name=Example Repository
   baseurl=http://repo.example.com
   enabled=1
   gpgcheck=1
   gpgkey=http://repo.example.com/gpgkey
   ```

---

#### **Section 3: GNU and Unix Commands**

9. **Answer**:  
   **B. `tail`**

10. **Answer**:  
    **Command**:  
    ```
    grep -i "error" /var/log/syslog | wc -l
    ```

11. **Answer**:  
    - **Hard Link**: Direct reference to the inode. Cannot cross filesystems. Created using `ln`.  
    - **Soft Link (Symbolic)**: Points to the file's path. Can cross filesystems. Created using `ln -s`.  

    **Example**:  
    ```
    ln file.txt hardlink.txt
    ln -s file.txt softlink.txt
    ```

12. **Answer**:  
    **Command**:  
    ```
    find /etc -name "*.conf" -mtime -7
    ```

13. **Answer**:  
    - **Cron**: A daemon for scheduling repetitive tasks.  
    **Example Cron Job**:  
    ```
    0 0 * * * /path/to/backup.sh
    ```

---

#### **Section 4: Devices, Filesystems, and FHS**

14. **Answer**:  
    **B. Disk usage in human-readable format**

15. **Answer**:  
    **Command**:  
    ```
    blkid
    ```

16. **Answer**:  
    - **ext3 vs ext4**:  
      - **Extents**: ext4 uses extents, reducing fragmentation.  
      - **Larger Volumes**: ext4 supports files up to 16TB and volumes up to 1EB.  
    - Ext3 is older and lacks ext4's performance enhancements.

17. **Answer**:  
    **Steps**:  
    1. Create a partition:  
       ```
       sudo fdisk /dev/sdX
       ```
    2. Format it:  
       ```
       sudo mkfs.ext4 /dev/sdX1
       ```
    3. Mount it:  
       ```
       sudo mkdir /data
       sudo mount /dev/sdX1 /data
       ```
    4. Make it permanent: Add to `/etc/fstab`:  
       ```
       /dev/sdX1  /data  ext4  defaults  0  2
       ```

18. **Answer**:  
    **Purpose of `/etc/fstab`**: Defines filesystems to be mounted at boot time.  
    **Example Entry**:  
    ```
    UUID=1234-5678  /data  ext4  defaults  0  2
    ```

---

#### **Bonus Question** *(Optional)*  

**Answer**:  
1. **BIOS/UEFI**: Initializes hardware and passes control to GRUB.  
2. **GRUB**: Loads the kernel and initial RAM disk (initrd).  
3. **Kernel**: Initializes hardware and mounts the root filesystem.  
4. **Init/Systemd**: Starts system services and processes.  

--- 
