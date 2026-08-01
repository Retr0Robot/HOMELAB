## Creating an Ubuntu live server VM on proxmox
How I installed Ubuntu live server vm on proxmox

## Goals 
Learn how to deploy other operating systems.
## Installation 
I first downloaded the ubuntu live server iso image from https://ubuntu.com/
I then uploaded the ubuntu download into the "iso images" tab on the "local pve"

I clicked "create vm", configured all of my preferred settings such as disk size and cpu cores I would like it to use, clicked finish and ran it.

I made sure everything was good and up to date "sudo apt-get update followed by sudo apt-get upgrade"

I installed the QEMU guest agent onto the ubuntu vm so that my pc (the host) and ubuntu (the guest operating system) has connection.
sudo apt-get install qemu-guest-agent


## Problems I ran into
Every time I would click start or run vm, the vm would open for a split second and then close immediately after.

## Solution
While spending around 30 mins trying to figure out the problem I learned that there is a node task history section! Which is an insanely valuable discovery!
I don't have any screen shots but there was a task error that stated TASK ERROR: "KVM virtualization configured, but not available. Either disable in VM configuration or enable in BIOS"

The entire time... Virtualization was not enabled in my BIOS.

Restarted my pc > enabled virtualization in BIOS > ran the VM again > AND IT WORKED!



## screenshots
I didn't take many screenshots 
<img width="1919" height="996" alt="Screenshot 2026-07-27 184605" src="https://github.com/user-attachments/assets/eee81760-a548-4168-b3e8-892b90bec9ca" />

<img width="645" height="262" alt="Screenshot 2026-07-31 210302" src="https://github.com/user-attachments/assets/3c8dae7c-524d-4be0-9035-fc4428ff372b" />

