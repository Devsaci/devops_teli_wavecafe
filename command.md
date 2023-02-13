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