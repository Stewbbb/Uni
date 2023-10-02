Memory management:
Programs request OS to allocate them memory through operating system call
The program is responsible for its own memory with more control than operating system




Virtual memory:
data and code sections 
The OS can page data from the memory to the disk so that more memory can be used by the program and only the pages that are being used need to be in ram, this means the program thinks it can access more memory than it actually can 
The buffer manager and memory mapping registers are used by OS to remember where each page is stored in physical memory


Memory management:
Runtime system provides either:
Explicit and implicit memory management:
Explicit:
C, C++:
C's runtime maintains its own data structure to organise memory it has obtained from operating system:
accessed by:
1. Malloc
	Allows program to request a contiguous amount of memory, If available this is recorded in the memory management data structure the address of the start of the block is returned to the program, if not available it requests more memory from OS
2. Free
	Given address of a block that was previous allocated and marks it available for future allocation

Disadvantages of Explicit:
	Program needs to keep track of every block requested with malloc so it can be freed later otherwise the program will have memory leaks, blocks of memory that can no longer be used or freed
	error is giving an address to free that had not been returned by malloc

Implicit:
Program language itself through runtime system provides mechanisms to allocate data structures and identifies allocated structures that can no longer be accessed by the program and adds it back into free memory
used by java, python etc.
Relieves heavy burden of keeping track of allocated memory from programmer

