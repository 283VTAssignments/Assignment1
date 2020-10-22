# Assignment1

Team members:
  Mamatha Guntu
  Arshia Sali
  
Contribution: We divided the MSR controls , took 2 each , coded and executed on our own VMs and later merged it in Git.
  Mamatha Guntu- Created VM, referred SDM for MSR controls - Primary ProcBased and VM-Exit controls. Coded and executed the code for them.
  Arshia Sali - Created VM, referred SDM for MSR controls - Secondary ProcBased and VM-Entry controls. Coded and executed the code for them.

Procedure
1. Install VMWARE WORKSTATION 16 PRO
2. Created a VM with Ubuntu 20.04.1-desktop ISO image file
3. Copy make and cmpe283-1.c file to the outer VM local folder 
4. Referred SDM VOL3 for MSR controls and their definitions
5. Create a macro for each control with their address
6. Create a structure with all of the MSR bit positions and their names
7. Run 'make' command to compile and build ,  a cmpe283-1.ko file is generated in the same folder
8. Insert this module into kernel using "sudo insmod ./ cmpe283-1.ko" 
9. Print message logs using "dmesg" command 

[11709.649221] CMPE 283 Assignment 1 Module Start
[11709.649225] Pinbased Controls MSR: 0x3f00000016
[11709.649226]   External Interrupt Exiting: Can set=Yes, Can clear=Yes
[11709.649227]   NMI Exiting: Can set=Yes, Can clear=Yes
[11709.649228]   Virtual NMIs: Can set=Yes, Can clear=Yes
[11709.649228]   Activate VMX Preemption Timer: Can set=No, Can clear=Yes
[11709.649228]   Process Posted Interrupts: Can set=No, Can clear=Yes

[11709.649229] Primary Procbased Controls MSR: 0xfff9fffe0401e172
[11709.649230]   Interrupt-window exiting: Can set=Yes, Can clear=Yes
[11709.649230]   Use TSC Offsetting: Can set=Yes, Can clear=Yes
[11709.649231]   HLT Exiting: Can set=Yes, Can clear=Yes
[11709.649231]   INVLPG Exiting: Can set=Yes, Can clear=Yes
[11709.649232]   MWAIT Exiting: Can set=Yes, Can clear=Yes
[11709.649232]   RDPMC Exiting: Can set=Yes, Can clear=Yes
[11709.649233]   RDTSC Exiting: Can set=Yes, Can clear=Yes
[11709.649233]   CR3-Load Exiting: Can set=Yes, Can clear=No
[11709.649234]   CR3-Store Exiting: Can set=Yes, Can clear=No
[11709.649234]   CR8-Load Exiting: Can set=Yes, Can clear=Yes
[11709.649234]   CR8-Store Exiting: Can set=Yes, Can clear=Yes
[11709.649235]   Use TPR Shadow: Can set=Yes, Can clear=Yes
[11709.649235]   NMI-Window Exiting: Can set=Yes, Can clear=Yes
[11709.649236]   MOV-DR Exiting: Can set=Yes, Can clear=Yes
[11709.649236]   Unconditional I/O Exiting: Can set=Yes, Can clear=Yes
[11709.649237]   Use I/O Bitmaps: Can set=Yes, Can clear=Yes
[11709.649237]   Monitor Trap Flag: Can set=Yes, Can clear=Yes
[11709.649238]   Use MSR Bitmaps: Can set=Yes, Can clear=Yes
[11709.649238]   MONITOR Exiting: Can set=Yes, Can clear=Yes
[11709.649238]   PAUSE Exiting: Can set=Yes, Can clear=Yes
[11709.649239]   Activate Secondary Controls: Can set=Yes, Can clear=Yes

[11709.649240] Secondary Procbased Controls MSR: 0x553cfe00000000
[11709.649240]   Virtualize APIC Accesses: Can set=No, Can clear=Yes
[11709.649241]   Enable EPT: Can set=Yes, Can clear=Yes
[11709.649241]   Descriptor-table Exiting: Can set=Yes, Can clear=Yes
[11709.649242]   Enable RDTSCP: Can set=Yes, Can clear=Yes
[11709.649242]   Virtualize x2APIC Mode: Can set=Yes, Can clear=Yes
[11709.649242]   Enable VPID: Can set=Yes, Can clear=Yes
[11709.649243]   WBINVD Exiting: Can set=Yes, Can clear=Yes
[11709.649243]   Unrestricted Guest: Can set=Yes, Can clear=Yes
[11709.649244]   APIC-register Virtualization: Can set=No, Can clear=Yes
[11709.649244]   Virtual-interrupt Delivery: Can set=No, Can clear=Yes
[11709.649245]   PAUSE-loop Exiting: Can set=Yes, Can clear=Yes
[11709.649245]   RDRAND Exiting: Can set=Yes, Can clear=Yes
[11709.649245]   Enable INVPCID: Can set=Yes, Can clear=Yes
[11709.649246]   Enable VM Functions: Can set=Yes, Can clear=Yes
[11709.649247]   VMCS Shadowing: Can set=No, Can clear=Yes
[11709.649247]   Enable ENCLS Exiting: Can set=No, Can clear=Yes
[11709.649247]   RDSEED Exiting: Can set=Yes, Can clear=Yes
[11709.649248]   Enable PML: Can set=No, Can clear=Yes
[11709.649248]   EPT-violation #VE: Can set=Yes, Can clear=Yes
[11709.649249]   Conceal VMX From PT: Can set=No, Can clear=Yes
[11709.649249]   Enable XSAVES/XRSTORS: Can set=Yes, Can clear=Yes
[11709.649250]   Mode-based Execution Control for EPT: Can set=Yes, Can clear=Yes
[11709.649250]   Sub-page write permissions for EPT: Can set=No, Can clear=Yes
[11709.649251]   Intel PT uses guest physical addresses: Can set=No, Can clear=Yes
[11709.649251]   Use TSC Scaling: Can set=No, Can clear=Yes
[11709.649251]   Enable user wait and pause: Can set=No, Can clear=Yes
[11709.649252]   Enable ENCLV exiting: Can set=No, Can clear=Yes

[11709.649253] Exit Controls MSR: 0x3fffff00036dff
[11709.649253]   Save Debug Controls: Can set=Yes, Can clear=No
[11709.649254]   Host address-space size: Can set=Yes, Can clear=Yes
[11709.649254]   Load IA32_PERF_GLOBAL_CTRL: Can set=Yes, Can clear=Yes
[11709.649255]   Acknowledge interrupt: Can set=Yes, Can clear=Yes
[11709.649255]   Save IA32_PAT: Can set=Yes, Can clear=Yes
[11709.649255]   Load IA32_PAT: Can set=Yes, Can clear=Yes
[11709.649256]   Save IA32_EFER: Can set=Yes, Can clear=Yes
[11709.649256]   Load IA32_EFER: Can set=Yes, Can clear=Yes
[11709.649257]   Save VMX Preemption Timer Value: Can set=No, Can clear=Yes
[11709.649257]   Clear IA32_BNDCFGS: Can set=No, Can clear=Yes
[11709.649258]   Conceal VMX from PT: Can set=No, Can clear=Yes
[11709.649258]   Clear IA32_RTIT_CTL: Can set=No, Can clear=Yes
[11709.649259]   Load CET state: Can set=No, Can clear=Yes
[11709.649259]   Load PKRS: Can set=No, Can clear=Yes

[11709.649260] Entry Controls MSR: 0xf3ff000011ff
[11709.649260]   Load Debug Controls: Can set=Yes, Can clear=No
[11709.649261]   IA-32e mode guest: Can set=Yes, Can clear=Yes
[11709.649261]   Entry to SMM: Can set=No, Can clear=Yes
[11709.649262]   Deactivate dual-monitor treatment: Can set=No, Can clear=Yes
[11709.649262]   Load IA32_PERF_GLOBAL_CTRL: Can set=Yes, Can clear=Yes
[11709.649262]   Load IA32_PAT: Can set=Yes, Can clear=Yes
[11709.649263]   Load IA32_EFER: Can set=Yes, Can clear=Yes
[11709.649263]   Clear IA32_BNDCFGS: Can set=No, Can clear=Yes
[11709.649264]   Conceal VMX from PT: Can set=No, Can clear=Yes
[11709.649264]   Load IA32_RTIT_CTL: Can set=No, Can clear=Yes
[11709.649265]   Load CET State: Can set=No, Can clear=Yes
[11709.649265]   Load PKRS: Can set=No, Can clear=Yes

10. Remove the module from the kernel with command "sudo rmmod ./ cmpe283-1.ko"
