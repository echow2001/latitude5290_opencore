# Dell Latitude 5290 2 in 1 OpenCore Configuration
opencore configuration for Dell Latitude 5290 2 in 1 hackintosh 


## credits: 
* https://github.com/laelsirus/Dell-Latitude-5290-2-in-1-CLOVER for some ACPI patches, graphics deviceproperties patches for kabylake 620 graphics
* https://dortania.github.io/OpenCore-Install-Guide/ 
* AirportItlwm
* Lilu
* VirtualSMC
* VoodooInput
* AppleALC

## installation
copy OC folder to your ESP, run opencore configurator to generate new SMBIOS( SN, ROM, UUID, MLB sn )

### notes
* If you have different NIC you may need to change the path `PciRoot(0x0)/Pci(0x1C,0x7)/Pci(0x0,0x0)` to your corresponding path for your NIC, or you may not need the built-in flag patched through OpenCore at all. You will also need different kexts if your card is not Intel.  
* Your boot drive may require different kext if it is SATA instead of NVMe

## working: 
* keyboard, mouse, usb
* thunderbolt
* graphical acceleration
* intel wifi + bt 
* imessage/icloud
* sound 
* cpu power mgmt/intel turbo
* battery status
* ... 

## not working
* sd reader
* wacom digitizer
* touchscreen
* fingerprint reader(if your machine has) 
* cameras
* thunderbolt hotplug 
* handoff/airdrop(can be working if you replace the nic) 
* you have to undock and dock the keyboard after a reboot or cold boot before itll start working for some reason
* ... 
