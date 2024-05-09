[konfig_MPLS_TE_IOS-XE_1]
-------------------------
1. Konfiguracja interfejsów
-------------------------




-------------------------
1. Konfiguracja interfejsów

# P1:
hostname P1

interface GigabitEthernet0/0
 description P1-P2
 ip address 10.1.2.1 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P1-P11
 ip address 10.1.11.1 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 1.1.1.1 255.255.255.255
 end


# P2:
hostname P2

interface GigabitEthernet0/0
 description P1-P2
 ip address 10.1.2.2 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/1
 description P2-P3
 ip address 10.2.3.2 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P2-P5
 ip address 10.2.5.2 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/4
 description P2-P7
 ip address 10.2.7.2 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 2.2.2.2 255.255.255.255
 end


# P3:
hostname P3

interface GigabitEthernet0/1
 description P2-P3
 ip address 10.2.3.3 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P3-P22
 ip address 10.3.22.3 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 3.3.3.3 255.255.255.255
 end


# P4:
hostname P4

interface GigabitEthernet0/0
 description P4-P7
 ip address 10.4.7.4 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/3
 description P4-P11
 ip address 10.4.11.4 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 4.4.4.4 255.255.255.255
 end


# P5:
hostname P5

interface GigabitEthernet0/0
 description P2-P5
 ip address 10.2.5.5 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/1
 description P5-P6
 ip address 10.5.6.5 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P5-P7
 ip address 10.5.7.5 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 5.5.5.5 255.255.255.255
 end


# P6:
hostname P6

interface GigabitEthernet0/1
 description P5-P6
 ip address 10.5.6.6 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/3
 description P6-P22
 ip address 10.6.22.6 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 6.6.6.6 255.255.255.255
 end


# P7:
hostname P7

interface GigabitEthernet0/0
 description P4-P7
 ip address 10.4.7.7 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P5-P7
 ip address 10.5.7.7 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/4
 description P2-P7
 ip address 10.2.7.7 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 7.7.7.7 255.255.255.255
 end


# PE11:
hostname PE11

interface GigabitEthernet0/0
 description PE11-CE1
 ip address 192.168.111.11 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/1
 description PE11-CE2
 ip address 192.168.112.11 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P1-PE11
 ip address 10.1.11.11 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/3
 description P4-PE11
 ip address 10.4.11.11 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 11.11.11.11 255.255.255.255
 end


# PE22:
hostname PE22

interface GigabitEthernet0/0
 description PE22-CE3
 ip address 192.168.223.22 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/1
 description PE22-CE4
 ip address 192.168.224.22 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/2
 description P3-PE22
 ip address 10.3.22.22 255.255.255.0
 no shut
 exit

interface GigabitEthernet0/3
 description P6-PE22
 ip address 10.6.22.22 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 22.22.22.22 255.255.255.255
 end


# CE1:
hostname CE1

interface GigabitEthernet0/0
 description PE11-CE1
 ip address 192.168.111.1 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 192.168.1.1 255.255.255.255
 end


# CE2:
hostname CE2

interface GigabitEthernet0/0
 description PE11-CE2
 ip address 192.168.112.2 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 192.168.1.2 255.255.255.255
 end


# CE3:
hostname CE3

interface GigabitEthernet0/0
 description PE22-CE3
 ip address 192.168.223.3 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 192.168.1.3 255.255.255.255
 end


# CE4:
hostname CE4

interface GigabitEthernet0/0
 description PE22-CE4
 ip address 192.168.224.4 255.255.255.0
 no shut
 exit

interface Loopback0
 ip address 192.168.1.4 255.255.255.255
 end
-------------------------