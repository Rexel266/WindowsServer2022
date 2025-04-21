This is for a Windows 11 host. To prepare the installatiom of Hyper-V on Windows 11 host, we need to make sure that the virtualization is enabled on the BIOS. I followed the below instructions.
---
1. Restart Computer
2. Pressed the appropriate key to go into BIOS/UEFI settings
3. Located the "Advanced" or "CPU Configuration" tab.
4. Look for options like "Intel Virtualization Technology" (VT-x), "AMD-V", or "Virtualization Technology".
5. Enabled the option and saved changes then reboot computer.
6. Upon loading of the computer, I have gone to the control panel > Programs and Features > Turn Windows Features on or off.
7. Enabled Hyper-V
  
![image](https://github.com/user-attachments/assets/43dfdd97-6f2b-468f-b101-eaee8a340754)

8. Reboot computer to apply updates.
9. Once done, Hyper-V will be installed.

---
Creation of virtual machine (Windows Server)

1. I downloaded the ISO file from the Windows Evaluation Center
2. Once downloaded, I opened the Hyper-V manager and hit on New.. > Virtual Machine
3. Specified the name of the VM (I set it as NuviaAD01) > Set the Generation to Generation 2 VM.
4. Set startup memory to 4 GB.
5. Set networking to not connected for now.
6. Set VHD to 20 GB (This is the allocation of hard drive space)
7. Set the installation options to a media.

![image](https://github.com/user-attachments/assets/149ce43f-e4ab-4d2c-953e-d6e7e788f1d5)

8. Once the VM is created, I started the VM to start the installation of Windows Server 2022.
9. Set local administrator credentials.
10. Back to Hyper-V manager, I disabled the checkpoint of the VM and set the Virtual Switch to Internal

---

Creation of virtual machine (Windows 10)
1. I downloaded the ISO file from the Windows Evaluation Center
2. Once downloaded, I opened the Hyper-V manager and hit on New.. > Virtual Machine
3. Specified the name of the VM (I set it as Nuviadsktp1) > Set the Generation to Generation 2 VM.
4. Set startup memory to 4 GB.
5. Set networking to not connected for now.
6. Set VHD to 75 GB (This is the allocation of hard drive space)
7. Set the installation options to a media and browsed to the ISO file I downloaded earlier.
8. Once the VM is created, I started the VM to start the installation of Windows 10.
9. Set local administrator credentials.
10. Back to Hyper-V manager, I disabled the checkpoint of the VM and set the Virtual Switch to Internal
