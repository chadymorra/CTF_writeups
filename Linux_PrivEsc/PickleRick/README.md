# Linux Box
---

### Nmap scan

```
22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.6 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
http-server-header: Apache/2.4.18 (Ubuntu)
http-title: Rick is sup4r cool
```
***Found username on source page***

**Username: R1ckRul3s**

*robots.txt has __Wubbalubbadubdub__ (password?)*

***Found login page /login.php***

*Found 1st ingredient*

*Found 2nd ingredient under /home/rick directory*

1. Used a php reverse shell in the commands section to open a shell
2. logged in as www-data
3. sudo -l shows that www-data may run everything as SUDO with NOPASSWORD
4. sudo bash -p give a root shell
**found 3rd ingredient under root home directory**

## Not alot of tricks here on this box, the usual nmap scan, gobuster directory enumeration, nikto to get the login.php path, looking at the html source code and robots.txt was necessary to find the username and password, and knowing how to get a reverse shell was needed as well. 
