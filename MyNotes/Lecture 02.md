# Booting Process Brief:
![](Pasted%20image%2020250520122705.png)

- Considering Soc given below. When CPU Powered on:![](Pasted%20image%2020250520123819.png)
- 
	1. `Program Counter` stores value of `reset vector` - this is default (Because it is the one that resets cpu)
	2. `reset vector` is located in `boot flash`
	3. reset vector jumps to the first instruction of bootloader software
	4. Bootloader initialised CPU RAM Controller.
# Kernel
Linux has Two different address spaces: `Kernel Space` and `User Space`
![](Pasted%20image%2020250520124941.png)
Basic Service is delivered by single executable, it's a monolithic kernel and Extendable Services (Loadable Kernel modules) are services required by run-time
# Device Tree
How does Kernel know Hardware at startup?
1. Have an integrated executable at the bootloader itself, takes more space, needs recompilation, takes more time. (Maybe ideal for microcontroller)
2. Provide to kernel at boot, meaning linking it to bootloader with a dedicated `Device Tree Blob` (DTB)
DTB is generated through Device Tree Source (DTS) or Hardware Definition to be precise, Only this can be recompiled when hardware changes are done.

# Root File System
Contains first user-level process (Initial RAM Disk `initrd`) 
![](Pasted%20image%2020250520131603.png)



