# kickstart
The purpose of this kickstart configuration file is the creation of a minimal Red Hat 8.6 build for use by Packer.  My environment doesn't allow for the self-hosted Packer solution, nor is there an available web server.  The customisation of the RHEL build is standard and includes both the ks.cfg and a modified isolinux.cfg

# Environment
* Windows 10 Home Edition 
* Windows Services for Linux 2 [1.1.3.0](https://learn.microsoft.com/en-us/windows/wsl/install)
  * Oracle Linux 8.5
  
* VMware Workstation 16 Player [16.2.5](https://docs.vmware.com/en/VMware-Workstation-Player-for-Windows/16.0/com.vmware.player.win.using.doc/GUID-B8509247-258C-4B11-8637-5DABACEA4965.html)
* Oracle VM VirtualBox Manager [7.0.6](https://www.virtualbox.org/manual/ch01.html#intro-installing)

# Kickstart Project : 

# Tools
``$create-gold-iso <name>``
  Examples : 

``$create-gold-iso v4``

``$create-gold-iso gold``
