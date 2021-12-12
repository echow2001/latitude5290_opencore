# latitude5290_opencore
opencore configuration for Dell Latitude 5290 2 in 1 hackintosh 


## credits: 
* https://github.com/laelsirus/Dell-Latitude-5290-2-in-1-CLOVER for ACPI patches, graphics deviceproperties patches
* https://dortania.github.io/OpenCore-Install-Guide/ 
* AirportItlwm
* Lilu
* VirtualSMC
* VoodooInput
* AppleALC

## installation
copy OC folder to your ESP, run opencore configurator to generate new SMBIOS( SN, ROM, UUID, MLB sn )

  note that the patch for built in network interface is specific to your installed network card. Dell ships this machine with multiple NICs and you are also free to install your own. If you have different card you may need to change the path `PciRoot(0x0)/Pci(0x1C,0x7)/Pci(0x0,0x0)` to your corresponding path for your NIC 
  Your boot drive may also require different kext if it is SATA instead of NVMe

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
* ... 
