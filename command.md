# PS C:\Users\Zakaria\DEVOPS_Imran Teli\wavecafe> vagrant init geerlingguy/centos7
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
PS C:\Users\Zakaria\DEVOPS_Imran Teli\wavecafe>

# PS C:\Users\Zakaria\DEVOPS_Imran Teli\wavecafe> vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'geerlingguy/centos7'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'geerlingguy/centos7' version '1.2.27' is up to date...
==> default: Setting the name of the VM: wavecafe_default_1676044866706_86814
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
    default: Adapter 2: hostonly
    default: Adapter 3: bridged
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection reset. Retrying...
    default: Warning: Connection aborted. Retrying...
    default: Warning: Remote connection disconnect. Retrying...
    default: Warning: Connection reset. Retrying...
    default: Warning: Connection aborted. Retrying...
    default: Warning: Connection reset. Retrying...
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 6.1.32
    default: VirtualBox Version: 7.0
==> default: Configuring and enabling network interfaces...
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/Zakaria/DEVOPS_Imran Teli/wavecafe
PS C:\Users\Zakaria\DEVOPS_Imran Teli\wavecafe>

# PS C:\Users\Zakaria\DEVOPS_Imran Teli\wavecafe> vagrant ssh
[vagrant@localhost ~]$ ls
[vagrant@localhost ~]$ ls al
ls: cannot access al: No such file or directory
[vagrant@localhost ~]$ ls -al
total 16
drwx------. 4 vagrant vagrant 111 Jan  5 04:02 .
drwxr-xr-x. 3 root    root     21 Jan  5 03:29 ..
drwx------. 3 vagrant vagrant  37 Jan  5 03:53 .ansible
-rw-r--r--. 1 vagrant vagrant  18 Apr  1  2020 .bash_logout
-rw-r--r--. 1 vagrant vagrant 193 Apr  1  2020 .bash_profile
-rw-r--r--. 1 vagrant vagrant 231 Apr  1  2020 .bashrc
drwx------. 2 vagrant vagrant  29 Feb 10 16:02 .ssh
-rw-r--r--. 1 vagrant vagrant   6 Jan  5 03:39 .vbox_version
[vagrant@localhost ~]$

# [vagrant@localhost ~]$ sudo -i
[root@localhost ~]# ls
anaconda-ks.cfg  original-ks.cfg
[root@localhost ~]#

# [root@localhost ~]# yum install httpd wget unzip -y
Loaded plugins: fastestmirror
Determining fastest mirrors
epel/x86_64/metalink                                                                    |  21 kB  00:00:00
 * base: mirror.in2p3.fr
 * epel: mirror.in2p3.fr
 * extras: mirror.in2p3.fr
 * updates: mirror.in2p3.fr
base                                                                                    | 3.6 kB  00:00:00
epel                                                                                    | 4.7 kB  00:00:00
extras                                                                                  | 2.9 kB  00:00:00
updates                                                                                 | 2.9 kB  00:00:00
(1/7): base/7/x86_64/group_gz                                                           | 153 kB  00:00:00
(2/7): extras/7/x86_64/primary_db                                                       | 249 kB  00:00:00
(3/7): epel/x86_64/group_gz                                                             |  99 kB  00:00:00
epel/x86_64/updateinfo         FAILED
https://ftp.plusline.net/epel/7/x86_64/repodata/dfd0328b896af73be35509c6fd832490a2c8e2aab19837670ee8ba66498d7fd4-updateinfo.xml.bz2: [Errno 14] HTTPS Error 404 - Not Found
Trying other mirror.
To address this issue please refer to the below wiki article

https://wiki.centos.org/yum-errors

If above article doesn't help to resolve this issue please use https://bugs.centos.org/.

(4/7): epel/x86_64/updateinfo                                                           | 1.0 MB  00:00:00
epel/x86_64/primary_db         FAILED                                          3.0 MB/s |  11 MB  00:00:07 ETA
https://mirror.karneval.cz/pub/linux/fedora/epel/7/x86_64/repodata/45408ec1d6e2881c46c9ae615352e36ef1222d467a21ed6228afcb970865e45e-primary.sqlite.bz2: [Errno 14] HTTPS Error 404 - Not Found
Trying other mirror.
(5/7): base/7/x86_64/primary_db                                                         | 6.1 MB  00:00:02
(6/7): epel/x86_64/primary_db                                                           | 7.0 MB  00:00:02
(7/7): updates/7/x86_64/primary_db                                                      |  19 MB  00:00:07
Package wget-1.14-18.el7_6.1.x86_64 already installed and latest version
Resolving Dependencies
--> Running transaction check
---> Package httpd.x86_64 0:2.4.6-98.el7.centos.6 will be installed
--> Processing Dependency: httpd-tools = 2.4.6-98.el7.centos.6 for package: httpd-2.4.6-98.el7.centos.6.x86_64
--> Processing Dependency: /etc/mime.types for package: httpd-2.4.6-98.el7.centos.6.x86_64
--> Processing Dependency: libaprutil-1.so.0()(64bit) for package: httpd-2.4.6-98.el7.centos.6.x86_64
--> Processing Dependency: libapr-1.so.0()(64bit) for package: httpd-2.4.6-98.el7.centos.6.x86_64
---> Package unzip.x86_64 0:6.0-24.el7_9 will be installed
--> Running transaction check
---> Package apr.x86_64 0:1.4.8-7.el7 will be installed
---> Package apr-util.x86_64 0:1.5.2-6.el7 will be installed
---> Package httpd-tools.x86_64 0:2.4.6-98.el7.centos.6 will be installed
---> Package mailcap.noarch 0:2.1.41-2.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

=============================================================================================================== Package                  Arch                Version                               Repository            Size
===============================================================================================================Installing:
 httpd                    x86_64              2.4.6-98.el7.centos.6                 updates              2.7 M
 unzip                    x86_64              6.0-24.el7_9                          updates              172 k
Installing for dependencies:
 apr                      x86_64              1.4.8-7.el7                           base                 104 k
 apr-util                 x86_64              1.5.2-6.el7                           base                  92 k
 httpd-tools              x86_64              2.4.6-98.el7.centos.6                 updates               94 k
 mailcap                  noarch              2.1.41-2.el7                          base                  31 k

Transaction Summary
===============================================================================================================Install  2 Packages (+4 Dependent packages)

Total download size: 3.2 M
Installed size: 10 M
Downloading packages:
(1/6): apr-util-1.5.2-6.el7.x86_64.rpm                                                  |  92 kB  00:00:00
(2/6): httpd-tools-2.4.6-98.el7.centos.6.x86_64.rpm                                     |  94 kB  00:00:00
(3/6): apr-1.4.8-7.el7.x86_64.rpm                                                       | 104 kB  00:00:02
(4/6): mailcap-2.1.41-2.el7.noarch.rpm                                                  |  31 kB  00:00:02
(5/6): unzip-6.0-24.el7_9.x86_64.rpm                                                    | 172 kB  00:00:02
(6/6): httpd-2.4.6-98.el7.centos.6.x86_64.rpm                                           | 2.7 MB  00:00:03
---------------------------------------------------------------------------------------------------------------Total                                                                          925 kB/s | 3.2 MB  00:00:03
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : apr-1.4.8-7.el7.x86_64                                                                      1/6
  Installing : apr-util-1.5.2-6.el7.x86_64                                                                 2/6
  Installing : httpd-tools-2.4.6-98.el7.centos.6.x86_64                                                    3/6
  Installing : mailcap-2.1.41-2.el7.noarch                                                                 4/6
  Installing : httpd-2.4.6-98.el7.centos.6.x86_64                                                          5/6
  Installing : unzip-6.0-24.el7_9.x86_64                                                                   6/6
  Verifying  : httpd-2.4.6-98.el7.centos.6.x86_64                                                          1/6
  Verifying  : mailcap-2.1.41-2.el7.noarch                                                                 2/6
  Verifying  : apr-1.4.8-7.el7.x86_64                                                                      3/6
  Verifying  : apr-util-1.5.2-6.el7.x86_64                                                                 4/6
  Verifying  : httpd-tools-2.4.6-98.el7.centos.6.x86_64                                                    5/6
  Verifying  : unzip-6.0-24.el7_9.x86_64                                                                   6/6

Installed:
  httpd.x86_64 0:2.4.6-98.el7.centos.6                       unzip.x86_64 0:6.0-24.el7_9

Dependency Installed:
  apr.x86_64 0:1.4.8-7.el7        apr-util.x86_64 0:1.5.2-6.el7   httpd-tools.x86_64 0:2.4.6-98.el7.centos.6
  mailcap.noarch 0:2.1.41-2.el7

Complete!
[root@localhost ~]#

# [root@localhost ~]# systemctl start httpd
[root@localhost ~]#

# [root@localhost ~]# systemctl enable httpd
Created symlink from /etc/systemd/system/multi-user.target.wants/httpd.service to /usr/lib/systemd/system/httpd.service.
[root@localhost ~]#

# [root@localhost ~]# ip addr show
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 08:00:27:03:5e:61 brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global noprefixroute dynamic enp0s3
       valid_lft 85240sec preferred_lft 85240sec
    inet6 fe80::a00:27ff:fe03:5e61/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
3: enp0s8: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 08:00:27:db:97:53 brd ff:ff:ff:ff:ff:ff
    inet 192.168.33.10/24 brd 192.168.33.255 scope global noprefixroute enp0s8
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fedb:9753/64 scope link
       valid_lft forever preferred_lft forever
4: enp0s9: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 08:00:27:fb:69:2c brd ff:ff:ff:ff:ff:ff
    inet 192.168.1.99/24 brd 192.168.1.255 scope global noprefixroute dynamic enp0s9
       valid_lft 85240sec preferred_lft 85240sec
    inet6 fe80::a00:27ff:fefb:692c/64 scope link
       valid_lft forever preferred_lft forever
[root@localhost ~]#

# [root@localhost ~]# ifconfig
enp0s3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:fe03:5e61  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:03:5e:61  txqueuelen 1000  (Ethernet)
        RX packets 30169  bytes 40817286 (38.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 5324  bytes 464414 (453.5 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp0s8: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.33.10  netmask 255.255.255.0  broadcast 192.168.33.255
        inet6 fe80::a00:27ff:fedb:9753  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:db:97:53  txqueuelen 1000  (Ethernet)
        RX packets 261  bytes 37808 (36.9 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 229  bytes 100401 (98.0 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp0s9: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.99  netmask 255.255.255.0  broadcast 192.168.1.255
        inet6 fe80::a00:27ff:fefb:692c  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:fb:69:2c  txqueuelen 1000  (Ethernet)
        RX packets 12239  bytes 765008 (747.0 KiB)
        RX errors 0  dropped 17  overruns 0  frame 0
        TX packets 741  bytes 56720 (55.3 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 72  bytes 6224 (6.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 72  bytes 6224 (6.0 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@localhost ~]#

# [vagrant@localhost ~]$ cd /var/www/html/
[vagrant@localhost html]$ ls
[vagrant@localhost html]$ ls -al
total 0
drwxr-xr-x. 2 root root  6 Jan 27 17:37 .
drwxr-xr-x. 4 root root 33 Feb 10 16:16 ..
[vagrant@localhost html]$

# [vagrant@localhost ~]$ sudo -i
# [root@localhost ~]# cd /var/www/html
[root@localhost html]# ls
[root@localhost html]# ls -al
total 0
drwxr-xr-x. 2 root root  6 Jan 27 17:37 .
drwxr-xr-x. 4 root root 33 Feb 10 16:16 ..
[root@localhost html]#

# PS C:\Users\Zakaria\devops_teli\wavecafe> vagrant ssh
Last login: Sun Feb 19 07:59:32 2023 from 10.0.2.2

[vagrant@localhost ~]$
# [vagrant@localhost ~]$ whoami
vagrant
# [vagrant@localhost ~]$ pwd
/home/vagrant
# [vagrant@localhost ~]$ cat /etc/os-release
NAME="CentOS Linux"
VERSION="7 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="7"
PRETTY_NAME="CentOS Linux 7 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:7"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"

CENTOS_MANTISBT_PROJECT="CentOS-7"
CENTOS_MANTISBT_PROJECT_VERSION="7"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="7"

[vagrant@localhost ~]$#

# [vagrant@localhost home]$ ls
vagrant
# [vagrant@localhost home]$ cd ..
[vagrant@localhost /]$ pwd
/
# [vagrant@localhost /]$ ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  vagrant  var
# [vagrant@localhost /]$ ls -al
total 24
dr-xr-xr-x.  18 root    root     239 Feb 10 16:02 .
dr-xr-xr-x.  18 root    root     239 Feb 10 16:02 ..
lrwxrwxrwx.   1 root    root       7 Jan  4 22:26 bin -> usr/bin
dr-xr-xr-x.   5 root    root    4096 Jan  5 04:02 boot
drwxr-xr-x.  19 root    root    3040 Feb 19 07:57 dev
drwxr-xr-x.  80 root    root    8192 Feb 19 07:58 etc
drwxr-xr-x.   3 root    root      21 Jan  5 03:29 home
lrwxrwxrwx.   1 root    root       7 Jan  4 22:26 lib -> usr/lib
lrwxrwxrwx.   1 root    root       9 Jan  4 22:26 lib64 -> usr/lib64
drwxr-xr-x.   2 root    root       6 Apr 11  2018 media
drwxr-xr-x.   2 root    root       6 Apr 11  2018 mnt
drwxr-xr-x.   3 root    root      39 Jan  5 04:01 opt
dr-xr-xr-x. 130 root    root       0 Feb 19 07:57 proc
dr-xr-x---.   3 root    root     170 Feb 10 21:21 root
drwxr-xr-x.  28 root    root     880 Feb 19 10:57 run
lrwxrwxrwx.   1 root    root       8 Jan  4 22:26 sbin -> usr/sbin
drwxr-xr-x.   2 root    root       6 Apr 11  2018 srv
dr-xr-xr-x.  13 root    root       0 Feb 19 07:57 sys
drwxrwxrwt.  11 root    root    4096 Feb 19 08:53 tmp
drwxr-xr-x.  13 root    root     155 Jan  4 22:26 usr
drwxrwxrwx.   1 vagrant vagrant 4096 Feb 13 17:45 vagrant
drwxr-xr-x.  20 root    root     278 Feb 10 16:16 var
# [vagrant@localhost /]$ cd /var/
# [vagrant@localhost var]$ ls
adm    crash  empty  gopher    lib    lock  mail  opt       run    tmp  yp
cache  db     games  kerberos  local  log   nis   preserve  spool  www
# [vagrant@localhost var]$ cd ..
# [vagrant@localhost /]$ cd /home/vagrant
# [vagrant@localhost ~]$ pwd
/home/vagrant
# [vagrant@localhost ~]$ sudo -i
# [root@localhost ~]# whoami
root
# [root@localhost ~]# pwd
/root
[root@localhost ~]#

# [vagrant@localhost ~]$ sudo -i
# [root@localhost ~]# whoami
root
# [root@localhost ~]# pwd
/root
# [root@localhost ~]# ls
anaconda-ks.cfg  original-ks.cfg
[root@localhost ~]#

# [root@localhost ~]# cd /
[root@localhost /]#

# [root@localhost /]# ls
bin   dev  home  lib64  mnt  proc  run   srv  tmp  vagrant
boot  etc  lib   media  opt  root  sbin  sys  usr  var
[root@localhost /]#

# [root@localhost /]# cd /bin/
# [root@localhost bin]# pwd
/bin
# [root@localhost bin]# ls
[                                   isosize                   readelf
a2p                                 jobs                      readlink
ab                                  join                      realpath
addr2line                           journalctl                recode-sr-latin
alias                               jp.py                     rename
apropos                             jp.py-2                   renice
ar                                  jp.py-2.7                 repoclosure
arch                                kbdinfo                   repodiff
as                                  kbd_mode                  repo-graph
aserver                             kbdrate                   repomanage
aulast                              kdumpctl                  repoquery
aulastlog                           kernel-install            repo-rss
ausyscall                           keyctl                    reposync
auvirt                              kill                      repotrack
awk                                 kmod                      reset
base64                              last                      resizecons
basename                            lastb                     rev
bash                                lastlog                   rm
bashbug                             lchfn                     rmail
bashbug-64                          lchsh                     rmail.postfix
bc                                  ld                        rmdir
bg                                  ld.bfd                    rpcgen
bond2team                           ldd                       rpm
bootctl                             ld.gold                   rpm2cpio
bunzip2                             less                      rpmdb
busctl                              lessecho                  rpmkeys
bzcat                               lesskey                   rpmquery
bzcmp                               lesspipe.sh               rpmverify
bzdiff                              lexgrog                   rsync
bzgrep                              link                      rsyslog-recover-qi.pl
bzip2                               linux32                   runcon
bzip2recover                        linux64                   run-parts
bzless                              linux-boot-prober         rvi
bzmore                              ln                        rview
c2ph                                loadkeys                  s2p
cal                                 loadunimap                scp
ca-legacy                           locale                    script
captoinfo                           localectl                 scriptreplay
cat                                 localedef                 sdiff
catchsegv                           logger                    secon
catman                              login                     sed
cd                                  loginctl                  seq
centrino-decode                     logname                   setarch
certutil                            logresolve                setcifsacl
c++filt                             look                      setfacl
chacl                               ls                        setfont
chage                               lsattr                    setkeycodes
chardetect                          lsblk                     setleds
chattr                              lscpu                     setmetamode
chcon                               lsinitrd                  setpriv
chfn                                lsipc                     setsid
chgrp                               lslocks                   setterm
chmem                               lslogins                  setup-nsssysinit
chmod                               lsmem                     setup-nsssysinit.sh
chown                               lsns                      setvtrgb
chronyc                             lsscsi                    sexp-conv
chrt                                lua                       sftp
chsh                                luac                      sg
chvt                                lz4                       sh
cifscreds                           lz4c                      sha1sum
cksum                               lz4cat                    sha224sum
clear                               machinectl                sha256sum
cmp                                 mailq                     sha384sum
cmsutil                             mailq.postfix             sha512sum
col                                 make                      show-changed-rco
colcrt                              makedb                    showconsolefont
colrm                               man                       show-installed
column                              mandb                     showkey
comm                                manpath                   shred
command                             mapscrn                   shuf
coredumpctl                         mcookie                   signver
cp                                  md5sum                    size
cpio                                mesg                      skill
cpupower                            mixartloader              slabinfo
crlutil                             mkdir                     slabtop
crontab                             mkfifo                    sleep
csplit                              mkinitrd                  slogin
csslint-0.6                         mknod                     snice
curl                                mktemp                    soelim
cut                                 modutil                   sort
cvtsudoers                          more                      sotruss
date                                mount                     splain
db_archive                          mountpoint                split
db_checkpoint                       msgattrib                 sprof
db_deadlock                         msgcat                    sqlite3
db_dump                             msgcmp                    ssh
db_dump185                          msgcomm                   ssh-add
db_hotbackup                        msgconv                   ssh-agent
db_load                             msgen                     ssh-copy-id
db_log_verify                       msgexec                   ssh-keygen
db_printlog                         msgfilter                 ssh-keyscan
db_recover                          msgfmt                    sshpass
db_replicate                        msggrep                   ssltap
db_stat                             msghack                   stat
db_tuner                            msginit                   stdbuf
db_upgrade                          msgmerge                  strings
dbus-binding-tool                   msgunfmt                  strip
dbus-cleanup-sockets                msguniq                   stty
dbus-daemon                         mv                        su
dbus-monitor                        namei                     sudo
dbus-run-session                    ndptool                   sudoedit
dbus-send                           needs-restarting          sudoreplay
dbus-test-tool                      neqn                      sum
dbus-update-activation-environment  netstat                   sync
dbus-uuidgen                        nettle-hash               systemctl
db_verify                           nettle-lfib-stream        systemd-analyze
dc                                  newaliases                systemd-ask-password
dd                                  newaliases.postfix        systemd-cat
deallocvt                           newgidmap                 systemd-cgls
debuginfo-install                   newgrp                    systemd-cgtop
df                                  newuidmap                 systemd-coredumpctl
dgawk                               nf-ct-add                 systemd-delta
diff                                nf-ct-list                systemd-detect-virt
diff3                               nf-exp-add                systemd-escape
dir                                 nf-exp-delete             systemd-firstboot
dircolors                           nf-exp-list               systemd-hwdb
dirname                             nf-log                    systemd-inhibit
dmesg                               nf-monitor                systemd-loginctl
dnsdomainname                       nf-queue                  systemd-machine-id-setup
domainname                          ngettext                  systemd-notify
dracut                              nice                      systemd-nspawn
du                                  nisdomainname             systemd-path
dumpkeys                            nl                        systemd-run
dwp                                 nl-addr-add               systemd-stdio-bridge
easy_install                        nl-addr-delete            systemd-sysv-convert
easy_install-2.7                    nl-addr-list              systemd-tmpfiles
echo                                nl-class-add              systemd-tty-ask-password-agent
egrep                               nl-class-delete           tabs
eject                               nl-classid-lookup         tac
elfedit                             nl-class-list             tail
env                                 nl-cls-add                tailf
envsubst                            nl-cls-delete             tar
eqn                                 nl-cls-list               taskset
ex                                  nl-fib-lookup             tbl
expand                              nl-link-enslave           teamd
expr                                nl-link-ifindex2name      teamdctl
factor                              nl-link-list              teamnl
fallocate                           nl-link-name2ifindex      tee
false                               nl-link-release           test
fc                                  nl-link-set               testgdbm
fg                                  nl-link-stats             tic
fgconsole                           nl-list-caches            timedatectl
fgrep                               nl-list-sockets           timeout
file                                nl-monitor                tload
find                                nl-neigh-add              tmon
find2perl                           nl-neigh-delete           toe
findmnt                             nl-neigh-list             top
find-repos-of-install               nl-neightbl-list          touch
fipscheck                           nl-pktloc-lookup          tput
fipshmac                            nl-qdisc-add              tr
firewall-cmd                        nl-qdisc-delete           tracepath
firewall-offline-cmd                nl-qdisc-list             tracepath6
flock                               nl-route-add              troff
fmt                                 nl-route-delete           true
fold                                nl-route-get              truncate
free                                nl-route-list             trust
funzip                              nl-rule-list              tset
gapplication                        nl-tctree-list            tsort
gawk                                nl-util-addr              tty
gdbus                               nm                        turbostat
gencat                              nmcli                     tzselect
genl-ctrl-list                      nm-online                 udevadm
geqn                                nmtui                     ul
getcifsacl                          nmtui-connect             umask
getconf                             nmtui-edit                umount
getent                              nmtui-hostname            unalias
getfacl                             nohup                     uname
getkeycodes                         nproc                     unexpand
getopt                              nroff                     unicode_start
getopts                             nsenter                   unicode_stop
gettext                             nss-policy-check          uniq
gettext.sh                          numfmt                    unlink
gio                                 objcopy                   unlz4
gio-querymodules-64                 objdump                   unshare
glib-compile-schemas                od                        unxz
gmake                               oldfind                   unzip
gneqn                               open                      unzipsfx
gnroff                              openssl                   update-ca-trust
gpasswd                             openvt                    update-mime-database
gpg                                 os-prober                 uptime
gpg2                                p11-kit                   urlgrabber
gpg-agent                           package-cleanup           users
gpgconf                             page_owner_sort           usleep
gpg-connect-agent                   passwd                    usx2yloader
gpg-error                           paste                     utmpdump
gpgparsemail                        pathchk                   uuidgen
gpgsplit                            pchrt                     VBoxClient
gpgv                                perl                      VBoxControl
gpgv2                               perl5.16.3                VBoxDRMClient
gpg-zip                             perlbug                   vdir
gpic                                perldoc                   verifytree
gprof                               perlthanks                vi
grep                                pflags                    view
groff                               pgawk                     vlock
grops                               pgrep                     vmstat
grotty                              pic                       vxloader
groups                              piconv                    w
grub2-editenv                       pinentry                  wait
grub2-file                          pinentry-curses           wall
grub2-fstest                        ping                      watch
grub2-glue-efi                      ping6                     watchgnupg
grub2-kbdcomp                       pinky                     wc
grub2-menulst2cfg                   pk12util                  wdctl
grub2-mkfont                        pkaction                  wget
grub2-mkimage                       pkcheck                   whatis
grub2-mklayout                      pkcs1-conv                whereis
grub2-mknetdir                      pkexec                    which
grub2-mkpasswd-pbkdf2               pkg-config                whiptail
grub2-mkrelpath                     pkill                     who
grub2-mkrescue                      pkla-admin-identities     whoami
grub2-mkstandalone                  pkla-check-authorization  write
grub2-render-label                  pkttyagent                x86_64
grub2-script-check                  pl2pm                     x86_energy_perf_policy
grub2-syslinux2cfg                  pldd                      xargs
gsettings                           plymouth                  xgettext
gsoelim                             pmap                      xmlcatalog
gtar                                pod2html                  xmllint
gtbl                                pod2man                   xmlwf
gtroff                              pod2text                  xz
gunzip                              pod2usage                 xzcat
gzexe                               post-grohtml              xzcmp
gzip                                powernow-k8-decode        xzdec
h2ph                                pr                        xzdiff
hdsploader                          preconv                   xzegrep
head                                pre-grohtml               xzfgrep
hexdump                             printenv                  xzgrep
hostid                              printf                    xzless
hostname                            prlimit                   xzmore
hostnamectl                         ps                        yes
htdbm                               psed                      ypdomainname
htdigest                            psfaddtable               yum
htpasswd                            psfgettable               yum-builddep
httxt2dbm                           psfstriptable             yum-config-manager
i386                                psfxtable                 yum-debug-dump
iconv                               pstruct                   yum-debug-restore
id                                  ptaskset                  yumdownloader
idiag-socket-details                ptx                       yum-groups-manager
idn                                 pwd                       zcat
igawk                               pwdx                      zcmp
info                                pwmake                    zdiff
infocmp                             pwscore                   zegrep
infokey                             pydoc                     zfgrep
infotocap                           python                    zforce
install                             python2                   zgrep
ionice                              python2.7                 zipgrep
ipcalc                              quota                     zipinfo
ipcmk                               quotasync                 zless
ipcrm                               ranlib                    zmore
ipcs                                raw                       znew
iptables-xml                        read                      zsoelim
[root@localhost bin]#

# [root@localhost bin]# cd /etc/
# [root@localhost etc]# ls
adjtime                  GREP_COLORS               modules-load.d     rsyncd.conf
aliases                  groff                     motd               rsyslog.conf
aliases.db               group                     mtab               rsyslog.d
alternatives             group-                    my.cnf             rwtab
anacrontab               grub2.cfg                 my.cnf.d           rwtab.d
asound.conf              grub.d                    netconfig          samba
audisp                   gshadow                   NetworkManager     sasl2
audit                    gshadow-                  networks           securetty
bash_completion.d        gss                       nfs.conf           security
bashrc                   gssproxy                  nfsmount.conf      selinux
binfmt.d                 host.conf                 nsswitch.conf      services
centos-release           hostname                  nsswitch.conf.bak  sestatus.conf
centos-release-upstream  hosts                     openldap           shadow
chkconfig.d              hosts.allow               opt                shadow-
chrony.conf              hosts.deny                os-release         shells
chrony.keys              httpd                     pam.d              skel
cifs-utils               idmapd.conf               passwd             ssh
cron.d                   init.d                    passwd-            ssl
cron.daily               inittab                   pkcs11             statetab
cron.deny                inputrc                   pki                statetab.d
cron.hourly              iproute2                  plymouth           subgid
cron.monthly             issue                     pm                 subuid
crontab                  issue.net                 polkit-1           sudo.conf
cron.weekly              kdump.conf                popt.d             sudoers
crypttab                 kernel                    postfix            sudoers.d
csh.cshrc                krb5.conf                 ppp                sudo-ldap.conf
csh.login                krb5.conf.d               prelink.conf.d     sysconfig
dbus-1                   ld.so.cache               printcap           sysctl.conf
default                  ld.so.conf                profile            sysctl.d
depmod.d                 ld.so.conf.d              profile.d          systemd
dhcp                     libaudit.conf             protocols          system-release
DIR_COLORS               libnl                     python             system-release-cpe
DIR_COLORS.256color      libuser.conf              rc0.d              tcsd.conf
DIR_COLORS.lightbgcolor  locale.conf               rc1.d              terminfo
dracut.conf              localtime                 rc2.d              tmpfiles.d
dracut.conf.d            login.defs                rc3.d              tuned
e2fsck.conf              logrotate.conf            rc4.d              udev
environment              logrotate.d               rc5.d              vconsole.conf
ethertypes               lvm                       rc6.d              virc
exports                  machine-id                rc.d               wgetrc
exports.d                magic                     rc.local           wpa_supplicant
favicon.png              mailcap                   redhat-release     X11
filesystems              makedumpfile.conf.sample  request-key.conf   xdg
firewalld                man_db.conf               request-key.d      xinetd.d
fstab                    mime.types                resolv.conf        yum
gcrypt                   mke2fs.conf               rpc                yum.conf
gnupg                    modprobe.d                rpm                yum.repos.d
[root@localhost etc]#