# Linux

```
pushd                                       # pushd _path_
dirs                                        # dirs
popd                                        # popd
eog                                         # eog input.png
```

```
lightdm                                     # lightdm --test-mode --debug
```


```
xournal                                     # echo "GTK+ Application for note taking"; echo "PDF Support"
simplescreenrecorder                        # echo "A feature-rich screen recorder that supports X11 and OpenGL"
axel                                        # axel -n 16 "https://oeis.org/stripped.gz"
httrack                                     # httrack -c8 "website_link"
wget                                        # wget --start-pos=OFFSET "https://oeis.org/stripped.gz"
curl                                        # curl -H "Header" "https://oeis.org/stripped.gz" 
cowsay/cowthink                             # fortune | cowsay
fortune                                     # echo "Print a random, hopefully interesting, adage"
ffmpeg                                      # ffmpeg -i input_video.mp4  -ss 00:26:48 -to 00:29:46 -vcodec libx264 -acodec aac -strict experimental -f mp4 out.mp4
```


```
objdump                                     # objdump -M intel -d x.out
readelf                                     # readelf -e a.out; echo "check man page"
```


```
gocr                                        # gocr -C 'A-Za-z' input.png
tesseract                                   # tesseract input.png stdout; echo "apt install tesseract-ocr"
mogrify                                     # mogrify -format ppm input.png; echo "check man page"
ocrad                                       # ocrad input.ppm
binwalk                                     # echo "Tool for searching binary images for embedded files and executable code"
dmd                                         # dmd input.d && ./input
gparted                                     # echo "GNOME Partition Editor for manipulating disk partitions"
gcc                                         # gcc input.c; ./a.out
g++                                         # g++ input.cpp; ./a.out
```

# Linux Info & Perf
- time _command_        # To time CPU/USER/Real time, CPU time can be bigger than real time (multi threading)
- cat /proc/cpuinfo
- cat /proc/meminfo
- cat /proc/ID/limits
- cat /proc/ID/numa_maps
- cat /proc/ID/sched
- cat /proc/ID/stat
- cat /proc/ID/statm
- cat /proc/ID/status 
- cat /proc/ID/maps  # Max in cat /proc/sys/vm/max_map_count
- sudo perf stat -d -d _command_
- sudo perf stat -e L1-dcache-loads,L1-dcache-load-misses _command_
- perf -h
- cat /proc/1/status | grep -i Vm
  - VmPeak: Peak virtual memory size.
  - VmSize: Current virtual memory size.
  - VmLck: Locked memory size (cannot be swapped out).
  - VmPin: Pinned memory size (pages that can't be moved).
  - VmHWM: Peak resident set size ("high water mark").
  - VmRSS: Resident set size (non-swapped physical memory).
  - VmData: Size of the data segment.
  - VmStk: Size of the stack.
  - VmExe: Size of the text segment.
  - VmLib: Shared library code size.
  - VmPTE: Page table entries size.
  - VmSwap: Swapped-out virtual memory size.
- echo 1/2/3 | sudo tee /proc/sys/vm/drop_caches
  - 1 Disk-Releated Cache Space
  - 2 dentries & i nodes
  - 3 for all
  - https://www.kernel.org/doc/Documentation/sysctl/vm.txt
- /proc/sys/fs/binfmt_misc    # Configrations for exetensions execution
- cat /proc/sys/fs/file-nr    # Number of Opened File Sys
- cat /proc/sys/fs/inode-nr   # Numer of Inodes and Free nodes (More in inode-state)
- iostat -d     # io state
- vmstat -s     # Memory Info with Description Including Pages
- top           # To see the cache/buffer that is emptied by drop_caches (Colored in htop)
- sar -d 5 2    # Disk stat after 5 second, two tries
- renice -n -10 -p _PID_
- mount -o remount,noatime /var/lib/mysql   # Remount SQL for Better Perf 
- SWAP:
  - dd if=/dev/zero of=/media/user/data/swap count=1K bs=200M # 200GB SWAP
  - sudo mkswap /media/user/data/swap 
  - sudo chown root:root /media/user/data/swap 
  - sudo chmod 600 /media/user/data/swap 
  - sudo swapon /media/user/data/swap


# Others 
- echo > /dev/tcp/192.168.1.1/80 && echo "Open"
- cat </dev/tty >k.txt

  
# TODO

- [ ] Terminal
- [ ] Builtin
- [ ] Apt Packages 
- [ ] /bin/
- [ ] .bashrc file 
- [ ] Welcome Message
- [ ] Apt Commands (apt, apt listing, apt-hold, add-apt, remove-apt, apt reset, apt-apt settings, apt-key, apt-file and LINK, )
- [ ] Kali 
- [ ] Grub
- [ ] init systemd service-file
- [ ] ircd and conf
- [ ] Research History File

# Temporary Listing ...

- arpspoof
- aircrack-ng
- adduser
- useradd
- bc
- diffpdf
- diff
- dpkg
- dex2jar
- fdisk
- lsof
- loggedfs
- ftp
- gdb
- git
- grep
- gradle
- gpg
- grub
- gzip and ... 
- hexedit
- hostname
- htop
- hwinfo
- traceroute
- ping
- nmap
- nslookup
- dig
- info
- man
- xinput
- init
- iptables
- xchat
- ircd-irc2
- john!
- modprobe and ...
- less
- lightdm
- linux-image linux-headers linux-modules
- lshw
- ltrace
- strace
- make
- maven
- mount
- nano
- net-tools and replacement
- ntfs-3g
- octave
- openssl
- passwd
- pdftk
- rar
- unrar
- python
- pip
- remmina
- xfreerdp
- rfkill
- dmesg
- sed
- awk
- simple-scan
- sqlitebrowser
- sshfs
- sudo and params
- tar
- tcpdump
- telnet
- time
- sleep
- ufw
- unzip
- wdiff
- whois
- wireshark
- xxd
- xmodmap
- 0
- 0
- type
- whereis
- whatis
- hash
- fg
- bg
- jobs
- history
- kill
- builtin
- umask
- unalias
- unset
- typeset
- ulimit
- trap
- script
- times
- source
- suspend
- printf
- read
- pwd
- readonly
- return
- set
- shift
- shopt
- logout
- local
- let
- eval
- echo
- enable
- disown
- declare
- complete
- compgen and ...
- bind
- command
- exec
- exit
- clear
- export
- getopts
- test
- caller
- mapfile
- help
- arpspoof
- file
- svn
- reboot
- shutdown
- xview and diff from eog
- convert and diff from mogrify
- update-grub
- md5sum
- shaXXsum
- sum
- systemctl
- startx and init and new desktop in diff session
- sudoedit
- xdg-open
- top
- htop
- chmod
- chown
- head
- tail
- stat
- ls and ...
- paste
- cut ... -d
- copy
- env
- which
- ! and shorts
- date
- more
- cp
- mv
- mkdir
- rm
- ps
- free
- ssh
- ifconfig
- route
- netstat
- ip # ip addr
- ssh keyfinger
- groups
- id
- chgrp
- w
- whoami
- who
- wc
- touch
- groupadd
- groupmod
- tac
- cat
- userdel
- grep with args
- deluser
- gzip
- gunzip
- sort
- xargs
- tr
