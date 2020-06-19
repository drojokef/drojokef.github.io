### RDTSCP
Intel Read Time-Stamp Counter(RDTSCP) on IA-32 and IA-64 Instruction Set Architectures at [rdtsc](https://gist.github.com/reaur/bacfd6d2b89d507d86959784bb99d627)

### ISPC
ispc compiles a C-based  [SPMD](https://en.wikipedia.org/wiki/SPMD) programming language to run on the SIMD units of CPUs and the Intel Xeon Phi™ architecture; it frequently provides a 3x or more speedup on CPUs with 4-wide vector SSE units and 5x-6x on CPUs with 8-wide AVX vector units, without any of the difficulty of writing intrinsics code.
You can download ispc on your machine at [Linux](https://github.com/ispc/ispc/releases/download/v1.13.0/ispc-v1.13.0-linux.tar.gz).

To access more details at [cppcon2016](https://www.youtube.com/watch?v=UgaQCg-0ZoU&t=330s)

### SC22 POSIX
SC22PAG N0005 Interim Report of the SC22 POSIX Advisory Group report at [OpenGroup](https://collaboration.opengroup.org/projects/sc22pag/documents/6511/SC22-PAG-N0005-interim.pdf).

### MMapedI/O
On modern operating systems, it is possible to mmap a file to a region of memory. When this is done, the file can be accessed just like an array in the program.
Memory mapping only works on entire pages of memory. Thus, addresses for mapping must be page-aligned, and length values will be rounded up. 

To determine the default size of a page the machine uses one should use: size_t page_size = (size_t) sysconf (_SC_PAGESIZE);

To access more details at [mmaped i/o](https://pages.mtu.edu/~soner/Classes/CS-3411/Slides/mmap.pdf)

