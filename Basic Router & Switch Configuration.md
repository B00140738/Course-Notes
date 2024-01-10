**Basic Router/Switch Configuration:**

**To switch from User mode to Privileged Exec mode**
Router>enable

**To switch to Global Configuration mode**
Router#configure terminal

**Set the hostname**
Router(config)#hostname R1

**Configure a banner:**
R1(config)#banner motd # No Unauthorized Access #

**Configure an interface**
R1(config)#interface gi 0/0
R1(config-if)#description Connection to xyz
R1(config-if)#ip address 192.168.1.1 255.255.255.0
R1(config-if)#no shutdown

**View interface configuration**
R1#show ip interface brief

**Configure the privileged exec password**
R1(config)#enable secret xyz123

**Configure the console password**
R1(config)#line console 0
R1(config-line)#password xyz123
R1(config-line)#login

**Configure the virtual lines password**
R1(config)#line vty 0 4
R1(config-line)#password xyz123
R1(config-line)#login

**Encrypt passwords**
R1(config)#service password-encryption
Disable DNS lookup
R1(config)#no ip domain-lookup

**Configure the switch management interface**
S1(config)#interface vlan 99
S1(config-if)#ip address 172.17.99.11 255.255.255.0
S1(config-if)#no shut

**Configure default gateway on switch**
S1(config)#ip default-gateway 172.17.99.1