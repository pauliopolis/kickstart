# kickstart
The purpose of this kickstart configuration file is the creation of a minimal Red Hat 8.6 build for use by Packer.  My environment doesn't allow for the self-hosted Packer solution, nor is there an available web server so here we first create a slightly customised ISO containing both the ks.cfg and a modified isolinux.cfg

# Environment
* Windows 10 Home Edition 
* Windows Services for Linux 2 [1.1.3.0](https://learn.microsoft.com/en-us/windows/wsl/install)
  * Oracle Linux 8.5
  
* VMware Workstation 16 Player [16.2.5](https://docs.vmware.com/en/VMware-Workstation-Player-for-Windows/16.0/com.vmware.player.win.using.doc/GUID-B8509247-258C-4B11-8637-5DABACEA4965.html)
* Oracle VM VirtualBox Manager [7.0.6](https://www.virtualbox.org/manual/ch01.html#intro-installing)

# Kickstart Project : 

# Tools

Not a particularly elegant script but used to reliably repeat the process of building the customised ISO and provided for convenience.

``$create-gold-iso <name>``

* Mounts the native RHEL 8.6 iso
* Copies (using rsync) the iso content to a build directory
* Copies in the isolinux.cfg and ks.cfg 
* Builds the customised iso
* Implants an MD5 checksum (keeping a readable copy)
  
  Examples : 

``$create-gold-iso v4``

``$create-gold-iso gold``

# isolinux.cfg

The menu and item titles are changed to make it clear this is a customised iso and the append line now points to the included ks.cfg (along with a few minor modifications).

# ks.cfg

Not much to say about this it's pretty standard stuff.  The packages that are included are specifically required by this environment to allow Packer to use ansible-local to install VBoxAdditions when creating a Vagrant BOX.  You will need to add your own root & vagrant user password hashes.

# Example

![image](https://user-images.githubusercontent.com/14337141/231193651-0d21fc17-d574-43a4-bde5-7d44fffec85c.png)

