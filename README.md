## Written by Sharon Tong
_________________________

### Contact
- Slack: @Sharon on wcscusf.slack.com
- LinkedIn: linkedin.com/in/sharon-tong
- Email: sharont1@mail.usf.edu
### Table of Contents
1. [Prerequisites](#id-link-to-section)
2. [Summary](#id-link-to-section)
3. [Installing PFsense](#id-link-to-section)
4. [Configuring PFsense](#id-link-to-section)
5. [Troubleshooting (optional)](#id-link-to-section)

## Prerequisites <a id="id-link-to-section"></a>
1. Have your [virtual environment](https://www.virtualbox.org/wiki/Downloads) configured
2. Have [WinRAR](https://www.win-rar.com/start.html?&L=0) installed on your computer.

## Summary <a id="id-link-to-section"></a>
PFsense is an open source firewall that is based on the FreeBSD operating system. Here we will learn how to install and setup PFsense in a virtualization software, in this case, VirtualBox.

## Installing PFsense <a id="id-link-to-section"></a>
1. Go to the PFsense download page [here](https://www.pfsense.org/download/)

2. Select the latest version of PFsense and the architecture you want based on the kind of CPU you have.
   If you have a 64-bit capable CPU, use the amd64 version (this works for Intel CPUs too). 
   If you have a 32-bit capable CPU, use the i386 version.

3. After it finishes downloading, open VirtualBox and click on 'New' on the upper left-hand corner. Type 'PFsense' into the 'Name' box,
   select BSD from the 'Type' dropdown menu, and select 'FreeBSD (64-bit)' or 'FreeBSD (32-bit) based on your CPU. Then click 'Next.'

![](createVM.png)

4. For RAM, I recommend at least 512 MB. Click 'next.'

![](memorySize.png)

5. For the virtual hard disk, the minimum is 2 GB, but if you are running low on hard disk space, you could get by with 1 GB. For those    who are planning on creating videos or performing extensive work within PFsense, select 6 GB. Here, I selected 4 GB to stay in the      middle.

![](createVirtualHardDisk.png)

6. Because the PFsense file we downloaded earlier is in the gz file format and VirtualBox does not support gz files, we will need an        application that will be able to extract content (the ISO file in our case, which VirtualBox does support) from gz files. In this        guide, we will be using WinRAR. Open the PFsense.iso.gz file in WinRAR and then select 'Extract To' at the top of the WinRAR screen.    I chose to extract the contents to my 'Downloads' folder. You can choose whichever folder you want.

![](extractISO.png)

Now that we have the ISO file, we can finish up the installation process.

8. Go back to VirtualBox. We will now place the PFsense ISO image file into VirtualBox so that our PFsense virtual machine will            recognize it and run PFsense.

   Go to 'Settings' on the upper left-hand corner of the VirtualBox screen. Then click on the 'Storage' tab. Click on 'Empty' under the    'Controller: IDE' section. Then click on the disc image and select 'Choose Virtual Optical Disk File...'

![](storingFile.png)

   Go to the location where you extracted the contents of the PFsense gz file to and select the PFsense ISO image file.

![](isoFileSuccess.png)

Congrats! You finished installing PFsense into VirtualBox! Next, we will cover configuration.

![](installSuccess.png) 

## Configuring PFsense <a id="id-link-to-section"></a>

## Troubleshooting (optional) <a id="id-link-to-section"></a>

##### Supporting detail (optional/ title name can change also)
group together logical ideas for the summary if needed
