### RDTSCP
Intel Read Time-Stamp Counter(RDTSCP) on IA-32 and IA-64 Instruction Set Architectures at [rdtsc](https://gist.github.com/reaur/bacfd6d2b89d507d86959784bb99d627)

### ISPC
ispc compiles a C-based  [SPMD](https://en.wikipedia.org/wiki/SPMD) programming language to run on the SIMD units of CPUs and the Intel Xeon Phi™ architecture; it frequently provides a 3x or more speedup on CPUs with 4-wide vector SSE units and 5x-6x on CPUs with 8-wide AVX vector units, without any of the difficulty of writing intrinsics code.
You can download ispc on your machine at [Linux](https://github.com/ispc/ispc/releases/download/v1.13.0/ispc-v1.13.0-linux.tar.gz).

To access more details at [cppcon2016](https://www.youtube.com/watch?v=UgaQCg-0ZoU&t=330s)

### MMapedI/O
On modern operating systems, it is possible to mmap a file to a region of memory. When this is done, the file can be accessed just like an array in the program.
Memory mapping only works on entire pages of memory. Thus, addresses for mapping must be page-aligned, and length values will be rounded up. 

To determine the default size of a page the machine uses one should use: size_t page_size = (size_t) sysconf (_SC_PAGESIZE);

To access more details at [mmaped i/o](https://pages.mtu.edu/~soner/Classes/CS-3411/Slides/mmap.pdf)

### Dynamic Kernel Linker (KLD) Facility
Allows the system administrator to dynamically add and remove functionality from a running system. This ability also helps software developers to develop new parts of the kernel without constantly rebooting to test their changes.

To access more details at [bsd](https://doc.lagout.org/security/Designing%20BSD%20Rootkits%20-%20An%20Introduction%20to%20Kernel%20Hacking.pdf)

### CHERI
CHERI (Capability Hardware Enhanced RISC Instructions) extends conventional processor Instruction-Set Architectures (ISAs) with architectural capabilities to enable fine-grained memory protection and highly scalable software compartmentalization.
CHERI is ISA with new security mechanisms.
-Fine-grained memory protection
-Scalable softaawre compartmentalization

CheriBSD is fork from FreeBSD and adapted to use of Cheri's new security mechanisms.

Fine-grained Memory Protection:

int x=1;

int secret_key=5000;

int main(){

int *p =&x;

p=p+1;

int leak = *p;

printf("Leak : %d\n",leak);

}

Pointers are typically compiled to just mechine addresses.
Pointer P originally pointed to x but it was increased by 1 and x is next to secret key in memory than points it.

With Cheri on the other hand, ponters can be compiled to capabilities.
Capabilitiy has an address, so still points to a memory location but it also has bounds information.
Whenever you try to use a capability(p=p+1) with an address that point outside its bound, hardware will trap.

To access more details at [Cheri](https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/)

### OpenBSD: Release Songs
[6.2: "A 3 line diff"](https://ftp.openbsd.org/pub/OpenBSD/songs/song62.mp3)

[6.1: "Winter of 95"](https://ftp.openbsd.org/pub/OpenBSD/songs/song61.mp3)

[6.0: "Another Smash of the Stack"](https://ftp.openbsd.org/pub/OpenBSD/songs/song60a.mp3)

[6.0: "Black Hat"](https://ftp.openbsd.org/pub/OpenBSD/songs/song60b.mp3)

[6.0: "Money"](https://ftp.openbsd.org/pub/OpenBSD/songs/song60c.mp3)

[6.0: "Comfortably Dumb"](https://ftp.openbsd.org/pub/OpenBSD/songs/song60d.mp3)

[6.0: "Mother"](https://ftp.openbsd.org/pub/OpenBSD/songs/song60e.mp3)

[6.0: "Goodbye"](https://ftp.openbsd.org/pub/OpenBSD/songs/song60f.mp3)

[6.2: "A 3 line diff"](https://ftp.openbsd.org/pub/OpenBSD/songs/song62.mp3)

[6.2: "A 3 line diff"](https://ftp.openbsd.org/pub/OpenBSD/songs/song62.mp3)

[6.2: "A 3 line diff"](https://ftp.openbsd.org/pub/OpenBSD/songs/song62.mp3)

[6.2: "A 3 line diff"](https://ftp.openbsd.org/pub/OpenBSD/songs/song62.mp3)

To access more details at [Release Songs](https://www.openbsd.org/lyrics.html)



