# squid4
<p>udah pada mamam belum? <br>
<p>mamam dulu atuh bisi salatri </p>
<p>I use ubuntu 15.04 in session to install this squid4<br>
my ip address proxy server  192.168.1.200<br>
dns-nameservers 192.168.1.1 gateway 192.168.1.1<br>
you can adjust or replace  ip address on the config below :<br>
-unbound.conf ---->  replace with the your IP address and domain <br>
-squid.conf ----> replace with your ip address<br>
-rc.local</p>

#repository by indonesia server
```bash
<p>local repostiroy ubuntu 15.04:
Indonesia-repository:
deb http://id.archive.ubuntu.com/ubuntu/ vivid main restricted universe multiverse
deb http://id.archive.ubuntu.com/ubuntu/ vivid-security main restricted universe multiverse 
deb http://id.archive.ubuntu.com/ubuntu/ vivid-updates main restricted universe multiverse
local-repository-Kambing.ui.ac.id:
deb http://kambing.ui.ac.id/ubuntu/ vivid main restricted universe multiverse
deb http://kambing.ui.ac.id/ubuntu/ vivid-updates main restricted universe multiverse
deb http://kambing.ui.ac.id/ubuntu/ vivid-security main restricted universe multiverse
deb http://kambing.ui.ac.id/ubuntu/ vivid-backports main restricted universe multiverse
deb http://kambing.ui.ac.id/ubuntu/ vivid-proposed main restricted universe multiverse
</p>
```
```
#installation
###already finish installation server,webserver
#install git
apt-get install git g++-4.4 -y
git clone https://github.com/puji122/squid4-autoinstall.git
cd squid4-autoinstall
chmod +x squid4.sh
./squid4.sh</p>
```

```
#after reboot 
delete dns-nameservers di /etc/network/interfaces or comment #dns-nameservers
/etc/init.d/networking restart
squid -k reconfigure
/etc/init.d/squid restart
/etc/init.d/unbound restart
dig google.com
unbound-control stats tail -16
tail -f /var/log/squid/access.log
```

```
#notification :
fyi install the package maintainer's version
choose : 
if the notification appears when installing software
```
