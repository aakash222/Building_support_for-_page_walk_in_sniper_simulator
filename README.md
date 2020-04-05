# Building_support_for-_page_walk_in_sniper_simulator
I have uploaded only files that needed to be changed in sniper simulator.
In sniper simulator whenever there is a tlb miss, it adds some fixed latency to the running time and doesn't do any 
address translation. In real systems, address translation latency is never constant.
For a four level page table, we may have to do different number of memory accesse (cache or RAM) for different address 
translations. For example, if physical address is found in tlb, then we don't need any memeory access (cache or RAM ).
If there is a hit in first level address translation cache(starting from root), we need three memory accesses. Similary if
there is hit in second level address translation cache, we need to do two memory accesses. similarly one memory access for
third level address translation cache hit. And fourth level address translation cache is our TLB itself.
In this project, we implemented page table and software page table walk. But, without adding address translation cache, every
time it was doing four memory accesses (cache or memory) for address translation. Then we implemented software address
translation cache for each level of the page table. After that we got different number of memory accesses for different address
translations.
