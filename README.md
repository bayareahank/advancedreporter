# advancedreporter
Automatically exported from code.google.com/p/advancedreporter

This code was finished and open sourced while I was working in Gear6, together with Rama. Gear6 was acquired by 
Violin Memory henceafter. 

It is a bit outdated now, there are a few things need to be done to make it up-to-date. 

1. Memcache protocol:    
   The current code works again memcache protocol 1.0, which utilize clear text for data transfer. It wasn't updated
   for the binary protocol. As I haven't kept track of progress on this side, there may be more to do in terms of 
   transfer protocol side. Though comparatively, binary data is easy to parse than text ones. 
   
2. Update to latest Kernel version:  
   As stated in the code, the code implemented in the form of kernel patch, is easy to port for kernels up to 2.6.25,
   up until the kernel name space is introduced (upon which concept Docker was built). There are also
   kernel link list and TCP/UDP table data structure updates in that version. The code needs to be updated to work on
   newer Kernel versions. 
   
3. The current code has an implementation bug, in how the kernel memeory is handled in the data aggregator part. 
   Sometimes this can trigger kernel into a freeze state for up to 4 seconds, as shown in a customer site. This bug
   was fixed internally, but wasn't updated to the open source site. Since Violin Memory has bought all the
   copyrights etc. from Gear6, you can inquire Violin Memory for the fix. 
   
Thanks. 

