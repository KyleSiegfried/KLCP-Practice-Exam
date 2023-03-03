**Chapter 1:**
	1.  A distribution based on Debian testing.

**Chapter 2:**
	1.  Kali 64-bit 
	2.  /proc/cpuinfo.
	3.  wget -q -O - [https://www.kali.org/archive-key.asc](https://www.kali.org/archive-key.asc) | gpg --import.
	4.  Installing from the official, validated Kali 32-bit ISO burned to USB 

**Chapter 3:**
	1.  ~
	2.  pwd, which, and type.
	3.  The file drwxr-xr-x 2 root root 60 Mar 21 08:30 vfio is not a block or character device.
	4.  The file permissions -r---w---- can be represented in octal notation as 204.
	5. Execute
	6.  kill %1.
	7.  chperm
	8.  id
	9.  lspci.
	10. /var

**Chapter 4:**
	1.  512 MB RAM / 2 GB hard drive free space
	2.  1024MB RAM GPU
	3.  False
	4.  True
	5.  Manual
	6.  Separate /home, /var, and /tmp partitions
	7.  Erase the boot loader and prevent Kali from booting
	8.  Provide predetermined answers to installation questions
	9.  Boot from an official, validated Kali ARM image and follow the installation steps
	10.  Save to floppy disk

**Chapter 5:**
	1.  NetworkManager
	2.  /etc/network
	3.  ifupdown
	4.  iface eth0 inet static
	5.  On the command line with ifupdown, On the command line with systemd-networkd, On the command line via the /etc/network/interfaces file, On the command line with .network files in the /etc/systemd/network directory, Graphically with NetworkManager
	6.  /etc/shadow
	7.  adduser
	8.  passwd -l olduser
	9.  The SSH service is installed by default, The default configuration file blocks certificate-based logins, The default keys from a live image are pre-generated
	10.  systemctl
	11.  createdb
	12.  pg_createuser
	13.  createdb -T template0 -E UTF-8 -O dbuser db_new
	14.  /var/www/html
	15.  All options are associated with Apache2
	16.  systemd
	17.  systemctl status postgresql

**Chapter 6:**
	1.  dpkg -s nmap | grep ^Version
	2.  reportbug
	3.  Use the official Debian bug tracker at [https://bugs.debian.org](https://bugs.debian.org/) and send an email (with a special syntax) to [submit@bugs.debian.org](mailto:submit@bugs.debian.org)

**Chapter 7:**
	1.  Pre-configured firewall enabled and all services rolled to non-default credentials
	2.  netfilter and iptables
	3.  INPUT
	4.  PREROUTING, INPUT, FORWARD, OUTPUT, POSTROUTING
	5.  MASQUERADE
	6.  iptables -A INPUT -s 8.8.8.8 -j DROP
	7.  iptables -F INPUT
	8.  iptables -A INPUT -p ssh -j ACCEPT or iptables -A INPUT --dport 22 -j ACCEPT or iptables -A INPUT --state NEW -p tcp --dport 22 -j ACCEPT or iptables -A INPUT -m state --state NEW -p tcp --dport 22 -j ACCEPT
	9.  /etc/netfilter.conf
	10.  gnome-system-monitor
	11.  dpkg -V
	12.  fail2ban

**Chapter 8:**
	1.  dpkg
	2.  Advanced Package Tool (apt)
	3.  /etc/apt/sources.list
	4.  deb [http://http.kali.org/kali](http://http.kali.org/kali) kali-rolling main non-free contrib
	5.  deb [http://http.kali.org/kali](http://http.kali.org/kali) kali-rolling main non-free contrib
	6.  kali-rolling
	7.  dpkg -i man-db_2.7.0.2-5_amd64.deb
	8.  apt-get full-upgrade
	9.  apt-get update
	10.  dpkg -L metasploit-framework
	11.  dpkg -S msfconsole
	12.  dpkg -l
	13.  dpkg --add-architecture
	14.  synaptic
	15.  dpkg --print-architecture
	16.  control.tar.gz
	17.  manifest
	18.  data.tar.xz
	19.  Breaks
	20.  postconf

**Chapter 9:**
	1.  apt source
	2.  git clone
	3.  apt build-dep ./
	4.  debian/changelog
	5.  dch --local kali
	6.  cp /boot/config-4.9.0-kali1-amd64/.config ~/kernel/linux-source-4.9/
	7.  make gconfig
	8.  apt install curl git live-build
	9.  # ./build.sh --arch amd64 --variant xfce --verbose
	10.  kali-linux-full
	11.  persistence.conf
	12.  mkfs.ext3 -L persistence /dev/sdc3
	13.  cryptsetup open --type LUKS /dev/sdb3 kali_persistence
	14.  cryptsetup luksAddNuke /dev/sdb4

**Chapter 10:**
	1.  (all)
	2.  salt '\*'pkg.install dnmap
	3.  salt kali-scratch cmd.shell ’uptime; uname -a’
	4.  dpkg-buildpackage -us -ub
	5.  reprepo
	6.  Codename, Architectures, Components
	7.  sources.list

**Chapter 11:**
	1.  Classification is not a part of the "CIA triad".
	2.  Availability will be the primary focus of the organization.
	3.  Confidentiality and integrity are affected by this flaw.
	4.  Exploit is the term used to describe software that can be used to take advantage of a security weakness.
	5.  Overall Risk provides guidance to those responsible for securing and maintaining the systems in question.
	6.  Penetration Test leverages identified issues to uncover the worst-case scenario.
	7.  Client-Side Attack is the technique used to target the various applications installed on the workstation of an employee within a target organization.
