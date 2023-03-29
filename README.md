# kickstart
Kickstart stuff

# Environment
* Windows 10 Home Edition 
* Windows Services for Linux 2 [1.1.3.0](https://learn.microsoft.com/en-us/windows/wsl/install)
  * Oracle Linux 8.5
  
* VMware Workstation 16 Player [16.2.5](https://docs.vmware.com/en/VMware-Workstation-Player-for-Windows/16.0/com.vmware.player.win.using.doc/GUID-B8509247-258C-4B11-8637-5DABACEA4965.html)
* Oracle VM VirtualBox Manager [7.0.6](https://www.virtualbox.org/manual/ch01.html#intro-installing)

# Kickstart Project : 

Create custom ISO with the kickstart file and modified boot loader menu to allow auto-installation without requirement to host the kicstart file elsewhere.

# Tools
``$create-gold-iso <name>``
  Examples : 
  $create-gold-iso v4
  $create-gold-iso gold (this is required if the iso will be used by packer subsequently)

