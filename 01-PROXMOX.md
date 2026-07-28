Setting up proxmox/installation 
--
Objective 
--
Install Proxmox VE to host virtual machines

## Hardware

- Seconday low end desktop
- 16 GB RAM
- 500 GB SSD
- 1tb external hard drive
- TP-link wifi router for somewhat of a firewall/security before I learn how to actually set one up 

## Steps

1. Downloaded Proxmox VE ISO
2. Flashed the ISO file onto my external hard drive using rufus
3. Installed Proxmox onto my seconday desktop using graphical install
4. Configured the server with my main desktop computer

## DHCP reservation
I logged into my tp link router which is what Proxmox is connected to, and I created a DHCP reservation for Proxmox so that the mac address ALWAYS gets the same IP address so I dont lose the location of Proxmox

## Created a backup drive for VM ISO files
I used the external hard drive that I flashed the Proxmox ISO on to, and plugged it into the pc running Proxmox
I wiped the disk of the ISO image by going into directory - created a directory - and formatted the external hard drive to ext4.
I clicked datacenter than storage and tried to add an NFS for backup.

## Problems with using the hard drive for backups
I thought I could just use my hard drive (i probably can) for the backups.
But there is no where to export the backups to since I was treating my external hard drive as a NAS device

## Solution
1.Either obtain a NAS device 

2.Reaserch how to use the external drive as my backup storage

## screenshots 

<img width="1919" height="1079" alt="proxhome" src="https://github.com/user-attachments/assets/2493f108-1025-48a3-ac83-5e898e7329a0" />


<img width="970" height="312" alt="dhcpres" src="https://github.com/user-attachments/assets/44f2438e-e13a-4bfa-ae70-6682997b4b15" />

   


