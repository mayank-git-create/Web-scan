# Install nmap
ubuntu@ubuntu-utm:~$ sudo apt-get install nmap
[sudo] password for ubuntu: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
nmap is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 1 not upgraded.
# Install apache2
ubuntu@ubuntu-utm:~$ sudo apt-get install apache2
Reading package lists... Done
Building dependency tree       
Reading state information... Done
apache2 is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 1 not upgraded.
# Install php5
ubuntu@ubuntu-utm:~$ sudo apt-get install php5
Reading package lists... Done
Building dependency tree       
Reading state information... Done
php5 is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 1 not upgraded.
ubuntu@ubuntu-utm:~$ php -v
PHP 5.5.9-1ubuntu4.29 (cli) (built: Apr 22 2019 18:33:52) 
Copyright (c) 1997-2014 The PHP Group
Zend Engine v2.5.0, Copyright (c) 1998-2014 Zend Technologies
    with Zend OPcache v7.0.3, Copyright (c) 1999-2014, by Zend Technologies
# Restart apache2
ubuntu@ubuntu-utm:~$ sudo service apache2 restart
 * Restarting web server apache2                                                
# Permissions
ubuntu@ubuntu-utm:~$ sudo chown ubuntu /var/www/html
ubuntu@ubuntu-utm:~$ sudo chmod 777 /var/www/html
ubuntu@ubuntu-utm:~$ sudo crontab -e
No modification made

ubuntu@ubuntu-utm:~$ /bin/nano
<? php

echo "Server Timestamp:";
echo date ("h:i:sa");

echo "<pre>"
include ("nmap.html");
echo "</pre>"
?>

Firefox

http://XXX.XXX.XX.X/network.php

Server Timestamp:08:34:19am

# Nmap 7.80 scan initiated Fri Aug 9 08:30:02 2024 as: nmap -oN /var/www/html/nmap.html XXX.XXX.XX.X/24 Nmap scan report for _gateway (XXX.XXX.XX.X) Host is up (0.00040s latency).

Not shown: 997 closed ports PORT STATE SERVICE 53/tcp open domain 5000/tcp open upnp 7000/tcp open afs3-fileserver MAC Address: A6:83:E7:22:5F:64 (Unknown)

Nmap scan report for ubuntu (XXX.XXX.XX.X) Host is up (0.000073s latency).

Not shown: 999 closed ports PORT STATE SERVICE 80/tcp open http

# Nmap done at Fri Aug

9 08:30:05 2024 -- 256 IP addresses (2 hosts up) scanned in 4.03 seconds

1 of 1

9/8/24, 4:39 pm

