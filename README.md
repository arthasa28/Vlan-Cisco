

# :pushpin: Vlan - Cisco Packet Tracer



<p align="center">
  <img src="https://i.postimg.cc/k5Wybw63/logo.jpg" alt="Logo Artha"/ style="height:350px;" "width: 350px;">
</p>


[![Version](https://img.shields.io/badge/VENOM-1.0.17-brightgreen.svg?maxAge=259200)]()
[![Stage](https://img.shields.io/badge/Release-Stable-brightgreen.svg)]()
![licence](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/aircrack-ng/badge.svg)](##Link##)



## :inbox_tray: Media Social Instagram

To keep this collection up-to-date need contributors who can add more Program Arduino scripts
||
|--------------|
|:mailbox_with_mail: [artha_sa_](https://www.instagram.com/artha_sa_/)


# :moneybag: [Donate](https://saweria.co/arthasyarif)

# :pushpin: Vlan - Cisco Packet Tracer



<p align="center">
  <img src="https://i.postimg.cc/k4Hk4pXs/Tabel1-Ip-1.png" alt="Contoh Artha"/ style="height:350px;" "width: 350px;">
  </br>
  <img src="https://i.postimg.cc/dVTmPNzv/Tabel1-Ip-2.png" alt="Contoh Artha"/ style="height:350px;" "width: 350px;">
  
</p>

## :loud_sound: Keterangan

- Config Dulu Switch Baru Router
- Port 24 Untuk Router
- Port 1 s/d Port 3 Untuk Vlan 10
- Port 3 s/d Port 15 Untuk Vlan 20
- Port 15 s/d Port 20 Untuk Vlan 30


# :clipboard: Source Config Switch

```bash

Switch>en
Switch#vlan database
Switch(vlan)#vlan 10 name VLAN10
VLAN 10 added:
    Name: VLAN10
Switch(vlan)#vlan 20 name VLAN20
VLAN 20 added:
    Name: VLAN20
Switch(vlan)#vlan 30 name VLAN30
VLAN 30 added:
    Name: VLAN30
Switch(vlan)#exit
APPLY completed.
Exiting....
Switch#show vlan

VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
10   VLAN10                           active    
20   VLAN20                           active    
30   VLAN30                           active    
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    

VLAN Type  SAID       MTU   Parent RingNo BridgeNo Stp  BrdgMode Trans1 Trans2
---- ----- ---------- ----- ------ ------ -------- ---- -------- ------ ------
1    enet  100001     1500  -      -      -        -    -        0      0
10   enet  100010     1500  -      -      -        -    -        0      0
20   enet  100020     1500  -      -      -        -    -        0      0
30   enet  100030     1500  -      -      -        -    -        0      0
1002 fddi  101002     1500  -      -      -        -    -        0      0   
1003 tr    101003     1500  -      -      -        -    -        0      0   
1004 fdnet 101004     1500  -      -      -        ieee -        0      0   
1005 trnet 101005     1500  -      -      -        ibm  -        0      0   

VLAN Type  SAID       MTU   Parent RingNo BridgeNo Stp  BrdgMode Trans1 Trans2
---- ----- ---------- ----- ------ ------ -------- ---- -------- ------ ------

Remote SPAN VLANs
------------------------------------------------------------------------------

Primary Secondary Type              Ports
------- --------- ----------------- ------------------------------------------

Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#int fa0/24
Switch(config-if)#switchport mode trunk
Switch(config-if)#no shut



*** VLAN 10 ***

Switch(config-if)#int fa0/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10

Switch(config-if)#int fa0/2
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10

Switch(config-if)#int fa0/3
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10



*** VLAN 20 ***

Switch(config-if)#interface fa0/4
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/5
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/6
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/7
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/8
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/9
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/10
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/11
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/12
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/13
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/14
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20

Switch(config-if)#int fa0/15
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20



*** VLAN 30 ***

Switch(config-if)#int fa0/16
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 30

Switch(config-if)#int fa0/17
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 30

Switch(config-if)#int fa0/18
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 30

Switch(config-if)#int fa0/19
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 30

Switch(config-if)#int fa0/20
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 30
Switch(config-if)#end
Switch#


```


# :clipboard: Source Config Router

```bash

         --- System Configuration Dialog ---

Would you like to enter the initial configuration dialog? [yes/no]: n


Press RETURN to get started!



Router>en
Router#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#int fa0/0
Router(config-if)#no shutdown

Router(config-if)#int fa0/0.10

Router(config-subif)#
Router(config-subif)#encapsulation ?
Router(config-subif)#encapsulation dot1q 10
Router(config-subif)#ip add 10.10.10.1 255.0.0.0

Router(config-subif)#int fa0/0.20
Router(config-subif)#encap dot1q 20
Router(config-subif)#ip add 20.20.20.1 255.0.0.0

Router(config-subuf)#int fa0/0.30
Router(config-subif)#encap dot1q 30
Router(config-subif)#ip add 30.30.30.1 255.0.0.0
Router(config-subif)#end


```
