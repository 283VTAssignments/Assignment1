# Assignment1

## Q1.

## Team members:
  - Mamatha Guntu
  - Arshia Sali
  
### Contribution: 
  We divided the MSR controls , took 2 each , coded and executed on our own VMs and later merged it in Git.

  - Mamatha Guntu- Created VM, referred SDM for MSR controls - Primary ProcBased and VM-Exit controls. Coded and executed the code for them.
  
  - Arshia Sali - Created VM, referred SDM for MSR controls - Secondary ProcBased and VM-Entry controls. Coded and executed the code for them.

## Q2.

### Procedure
1. Install VMWARE WORKSTATION 16 PRO
2. Created a VM with Ubuntu 20.04.1-desktop ISO image file
3. Copy make and cmpe283-1.c file to the outer VM local folder 
4. Referred SDM VOL3 for MSR controls and their definitions
5. Create a macro for each control with their address
6. Create a structure with all of the MSR bit positions and their names
7. Run 'make' command to compile and build ,  a cmpe283-1.ko file is generated in the same folder
8. Insert this module into kernel using "sudo insmod ./ cmpe283-1.ko" 
9. Print message logs using "dmesg" command 
10. Remove the module from the kernel with command "sudo rmmod ./ cmpe283-1.ko"
