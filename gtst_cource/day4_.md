# *Further on Linux*
## Linux File Hierarchy
- Linux/UNIX have a special  file system than windows.
- File system is a directory structure that the OS uses.
- Windows: System files appear under the local disk C:
- Linux: System files appear under the rootdirectory ( /)
## File structure in detail
### 1./ ( root )
- Every single file and directory starts from the root directory
- The only root user has the right to write under this directory
- /root is the root user’s home directory, which is not the same as /
### 2./bin - Binary executables
- Essential command binaries that need to be available in single-user mode; for all users 
  - e.g cat, ls, cp,pwd 
### 3./boot - Boot loader files
- Kernel initrd, vmlinux, grub files are located under /boot
  - Example: initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-generic
### 4./dev - Essential Device files
- These include terminal devices, usb, or any device attached to the system.
  - Example: /dev/tty1, /dev/usbmon0
### 5./etc - et cetera
- Contains configuration files required by all programs.
- This also contains startup and shutdown shell scripts used to start/stop individual programs.
 - Example: /etc/resolv.conf, /etc/logrotate.conf.
### 6./home - Home directory
- Home directories for all users to store their personal files.
  - example: /home/nathan, /home/rexder
### 7./lib - Libraries essential for the binaries in /bin & /sbin
- Library filenames are either ld* or lib*.so.*
  - Example: ld-2.11.1.so, libncurses.so.5.7
### 8./media - Mount points for removable media such as CD-ROMs
- Temporary mount directory for removable devices.
  - Examples, /media/cdrom for CD-ROM; /media/floppy for floppy drives; /media/cd recorder for CD writer
### 9./mnt - Temporarily mounted file
- Temporary mount directory where sysadmins can mount filesystems.
### 10./opt - Optional application software packages
- Contains add-on applications from individual vendors.
- Add-on applications should be  installed under either /opt/ or /opt/ sub-directory.
### 11./sbin - Essential system binaries
- Just like /bin, /sbin also contains binary executables.
- The linux commands located under this directory are used typically by system administrator, for system maintenance purpose.
### 12./tmp - Temporary Files
- Directory that contains temporary files created by system and users.
- Files under this directory are deleted when system is rebooted.
### 13./usr - User Utilities
- Contains binaries, libraries, documentation, and source-code for second level programs.
- /usr/bin contains binary files for user programs. If you can’t find a user binary under /bin, look under /usr/bin. For example: at, awk, cc, less, scp
- /usr/sbin contains binary files for system administrators. If you can’t find a system binary under /sbin, look under /usr/sbin. For example: atd, cron, sshd, useradd, userdel
- /usr/lib contains libraries for /usr/bin and /usr/sbin
- /usr/src holds the Linux kernel sources, header-files and documentation.
## Text Editors
- Programs That user for text processing.
- Linux command line text editors
  - VIM
  - Nano
  - Emacs
  - Neovim
  -  ….
- Linux Graphical Text editors
  - Sublime
  - Vscode
  - Gedit
  - Pluma
  - …
## VIM
- Vim is a text editor for Unix that comes with Linux, BSD, and macOS. It is known to be fast and powerful, partly because it is a small program that can run in a terminal (although it has a graphical interface). It is mainly because it can be managed entirely without menus or a mouse with a keyboard.
- Vim is a text editor that is an upgraded version of the Vi editor and is more compatible with Vi. The most usage of vi editors is to create a new file, edit an existing file, or just read a file. Vim editor is more useful in editing different kinds of plain text. This command is more used in editing programs.
- Vim is by default on command mode when you open it.
- To get on insert mode you have to type ‘i’
- vim file
#### Inside Command mode you can
- Save ->  :w +
- Save & quit -> :wq
- Force Quit & Save
- Undo ->:undo + or :u
- Execute bash commands
## NANO
- GNU nano  is a simple terminal-based text editor. Though not as powerful as Emacs or Vim, it is easy to learn and use. Nano is ideal for making small changes to existing configuration files or for writing short plain text files.
- is a user-friendly, free and open-source text editor that usually comes pre-installed in modern Linux systems.
- nano filename
#### Saving Exiting & Undo_redo
- Ctrl + S - save
- Alt + U - Undo 
- Alt + E - Redo
- Ctrl + X - Exit
- Paste,Copy & paste all over the linux is
- Ctrl+shift+C - copy
- Ctrl+shift+X - Cut
- Ctrl+shift+V - Paste 
- the ^ is equal to ‘Ctrl’
## Linux User Management
- On Computer system, person who uses the computer is called “user”
- Every Users have Group.
- Users have their own file & applications.
- To know our name on linux -> “ whoami “
-  Those users have power/privilege.
- On linux there's 2 kinds users.
  - Root id = 0
  - Normal User id start with 1-999
-The root user have the power to do everything on linux , but if users want to have a root access they add sudo in front of the command .
- SUDO = Superuser do , used to pass permission denied
## Creating Users
- On linux, to create users you can use the following commands
  - Useradd -> simple 
  - Adduser -> Detailed
- Useradd command
  - sudo useradd username
- Adduser command
  - sudo adduser username
- The User files are stored inside /etc/passwd
- The User password are stored inside /etc/shadow
- When you create a user it creates a group with that name.
## To access root user
- command: is sudo su
