# Network-Security-Project

### Topology:
![Screenshot (10)](https://github.com/user-attachments/assets/a985e8e1-f5a0-4c29-b220-b5f083a65410)


# this project contaion :

## basic configuration like
  - routing "OSPF"
  - subnetting 
  - switching
  - wireless
  - DHCP
  - encrypt password
  - ssh configuration
  - all rechability configration
  - natting

## Security configuation 
  - ASA cisco firewall
  - IPS
  - VPN
  - zone transfer security
  - ACL  "access control list"
  - privilage user 
  - layer 2 security
  - port security
  - DAI  "dynamic arp incpection"
  - DHCP spoofing
  - STP  "spanning tree"
  - 802.1x security
  - tacaces server authentication
  - radious server authentication
  - vlan security
  - svi security
  - ospf authentication
  - wireless security

---------------------------------------------------------------------------------

Depend in this project by subnating use /27 because thats all we need to spluyment all network on topology
and use the last network in this subnet and divided them into /30 because used between the routers and in loop back because save the all rang of the ip i have 

## /27 subnet

To subnet the network 192.168.10.0/24 into /27 subnets, we'll break down the address space as follows:

Step 1: Understanding the /27 Subnet Mask
Original network: 192.168.10.0/24 (Subnet Mask: 255.255.255.0)
New subnet mask: /27 (Subnet Mask: 255.255.255.224)
Step 2: Determine Subnet Details
Number of subnets: Going from /24 to /27 increases the number of bits for subnetting by 3 (from 24 to 27), which gives us 

![Screenshot (12)](https://github.com/user-attachments/assets/147b16b3-c238-4375-9bed-558e7716fc56)
---------------------------------------------------------------------------------

## /30 subnet
Step 1: Understanding the /30 Subnet Mask
Original subnet: 192.168.10.224/27 (Subnet Mask: 255.255.255.224)
New subnet mask: /30 (Subnet Mask: 255.255.255.252)
Step 2: Determine Subnet Details
Number of subnets: Going from /27 to /30 increases the number of bits for subnetting by 3 (from 27 to 30), giving us 

![Screenshot (13)](https://github.com/user-attachments/assets/d631c4fc-2b87-45db-829e-2048c7115d26)
---------------------------------------------------------------------------------

## Details for topology network 😊
### Router 1 network
contain :
 - layer 2 security
 - svi security
 - vlan security
 - DAI dynamic arp incpection
 - port security
 - 3 vlan on 3 interface
 - 2 differnt vlan on differnt switch
---------------------------------------------------------------------------------

### Router 2 network
contain :
 - tacacs server on all the routers and networks
 - radus server on all the routers and networks
 - syslog server
 - ntp server
 - 802.1x security
 - connect with ASA firewall
---------------------------------------------------------------------------------

### Router 3 network 
contain :
  - ips Indrusion prevention system
  - no on can access th incide ips network
  - any one in ips an access outside
---------------------------------------------------------------------------------

### Router 4 network
contain :
  - zone policy security
  - port security manual & sticky
---------------------------------------------------------------------------------

### Router1 & Router4
  - between them contain the VPN connection with encrpted tunneling
---------------------------------------------------------------------------------

### ASA cisco firewall
contain :
  - 3 zone in security policy
  - inside & outside & dmz
  - dmz zone contain the web server
  - the inside zone can access dmz
  - the incide can access outside
