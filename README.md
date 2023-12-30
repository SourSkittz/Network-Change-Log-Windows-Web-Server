# Network-Change-Log-Windows-Web-Server
Network Change Log Windows Web Server
Network Configuration 

Windows Webserver
Open Network and Sharing Center 
Change adapter settings
Right-click Ethernet0 and click properties 
Internet Protocol Version 4 
IP Address: 10.0.1.00
Subnet Mask: 255.0.0.0
Default Gateway 10.0.1.2

Windows AD-DNS
Open Network and Sharing Center 
Manage network connections
Right-click Local Area Connection 2 and click properties 
Internet Protocol Version 4 
IP Address: 192.168.1.5
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.1.1

Windows 10 
Open Network and Sharing Center 
Change adapter settings
Right-click Ethernet0 and click properties 
Internet Protocol Version 4 
IP Address: 192.168.1.100
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.1.1

Vyatta Router WAN
Login into router
Sudo nano /etc/network/interfaces
Eth3 (external) 
IP address: 10.100.4.5
Netmask: 255.0.0.0
Network: 10.0.0.0
Broadcast: 10.255.255.255
Eth2 (internal) 
IP address: 172.31.0.9
Netmask: 255.255.0.0
Network: 172.31.0.0
Broadcast: 172.31.255.255

Vyatta Router LAN
Login into router
Sudo nano /etc/network/interfaces
Eth2 (external) 
IP address: 192.168.6.1
Netmask: 255.255.255.0
Network: 192.168.6.2
Broadcast: 192.168.6.255
Eth3 (internal) 
IP address: 192.169.1.1
Netmask: 255.255.255.0
Network: 192.168.1.0
Broadcast: 192.168.1.255

RHEL Database Server
nmtui edit ens192
Addresses: 10.0.1.200/24
Gateway: 10.0.1.2

RHEL Client
nmtui edit ens192 
Addresses: 192.168.1.101/24
Gateway: 192.168.1.1

PFSense Firewall
Login
Select option 2 (set interfaces IP address)
Enter the interface you wish to configure (WAN=1, Sunscreen=2, INTTOPF=3)
Configure IPv4 address via DHCP? Enter no
Enter IP address
Enter subnet mask as either 8, 16, or 24
WAN
172.31.0.15/16
Subscreen
10.0.1.2/24
INTTOPF
182.168.6.2/24

Kali 
Sudo nano /etc/network/interfaces 
Eth0 
Address: 172.31.0.6
Netmask: 255.255.0.0
Gateway: 172.31.0.9

How Devices can Communicate with each other

Windows AD-DNS is able to ping the Router LAN, Windows 10, and Red Hat systems. But is not able to ping outside the network to the Firewall or other devices outside the internal LAN. It can ping the 192.168.6.1 IP address.

Windows 10 is able to ping the Router LAN, Windows AD-DNS, and Red Hat systems. But is not able to ping outside the network to the Firewall or other devices outside the internal LAN. It cannot ping the 192.168.6.1 IP address.

Red Hat is able to ping the Router LAN, Windows 10, and Windows AD-DNS systems. But is not able to ping outside the network to the Firewall or other devices outside the internal LAN. It can ping the 192.168.6.1 IP address.

Router LAN is able to ping the Windows 10, Red Hat, and Windows AD-DNS systems. But the Router LAN is able to ping the Firewall’s LAN, DMZ, and WAN IP addresses. It is also able to ping into the screened subnet to the Windows Webserver and RHEL Database. The Router LAN is able to ping the Router WAN’s IP address of 172.31.0.9 but not the IP address of 10.100.4.5. 

Windows Web Server is able to ping the RHEL Database and the Firewall’s LAN, DMZ, and WAN IP addresses. The Windows Web Server is able to ping Router LAN’s IP address of 192.168.6.1 but not the internal LAN IP address of 192.168.1.1 and its systems. Windows Web Server is not able to ping Router WAN’s IP addresses of 172.31.0.9 and 10.100.4.5. 

RHEL Database is able to ping the Windows Web Server and the Firewall’s LAN, DMZ, and WAN IP addresses. The RHEL Database is able to ping Router LAN’s IP address of 192.168.6.1 but not the internal LAN IP address of 192.168.1.1 and its systems. RHEL Database is not able to ping Router WAN’s IP addresses of 172.31.0.9 and 10.100.4.5. 

Firewall is able to ping Router LAN’s 192.168.6.1 IP address but not the internal LAN’s IP address of 192.168.1.1 and its systems. Firewall is able to ping into the screened subnet and ping the Windows Web Server and RHEL Database systems. Firewall is able to ping Router WAN’s IP address of 172.31.0.9 but not its IP address of 10.100.4.5. 

Router WAN is able to ping the Firewall WAN’s IP address but nothing else. 


Admin, User, and Guest Accounts for Windows and Linux

Administrator Account
	Username: Admin
	Password: 0nlyPh@nsCo

David User Account 
	Username: David
	Password: D0ntC0m3!n

Ashli User Account
Username: Ashli
	Password: D0ntC0m3!n

Garrett User Account
	Username: Garrett
	Password: D0ntC0m3!n

Guest Account
	Username: Guest 








Change Log Form















VISIO Diagram 








ONLY FANS YOU NEED BUSINESS
3 GOODS:

Ceiling fan $149.99
Get your ceiling fan to cool down any room perfect for living rooms and bedrooms.

Standard fan (19.99)
This fan is perfect for use as it is small and compact and can be taken everywhere. Set it up anywhere where you could be standing still for long periods of time.

Air-Purifying Fans ($299.99)
For our most exclusive and special fans, we have an air-purifying cooling fan that even removes dust particles for all your allergenic needs. This fan also rotates and is perfect to put into any room to instantly cool it down.

3 SERVICES:
Fan installation Service - 
For any installation needs such as mounting fans or putting in the ceiling fan, our team will be more than happy to help any customers in need.
Delivery - 
We have delivery options with express/same day for an additional fee, but our standard delivery time will be about 4-6 business days.
Warranty - 
If you want to get the only fans subscription to any of our beautiful fan models, there is a warranty in case the fans cease to work.

Website
https://onlyfansyouneed.wordpress.com/ 




Project Requirements List




Automate Admin Tasks




















Appropriate Software to do Work


















Vulnerability Scanner Installed 


