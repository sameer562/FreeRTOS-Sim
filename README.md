# FreeRTOS-Sim
FreeRTOS simulator for POSIX (Linux, OS X and maybe other POSIX OS)

Based on the Linux simulator originally developed by William Davy, the goal of this work is to keep FreeRTOS POSIX simulator in a clean seperate package and up to date with the latest FreeRTOS releases.

Directory description
- Source: FreeRTOS kernel and POSIX simulator source files
- Project: the project directory that includes main() and FreeRTOS settings for the POSIX port
- Demo: demo tasks from the official FreeRTOS release

### Note
V10 is added to the master branch without extensive tests. Feel free to report or fix bugs.



### Errors may face during its compilation:
It showed the below error during compilation :

>> Compiling croutine.c
In file included from /usr/include/stdint.h:25:0,
                 from /usr/lib/gcc/x86_64-linux-gnu/5/include/stdint.h:9,
                 from /home/vsameer1/Downloads/FreeRTOS-Sim-master/Source/include/FreeRTOS.h:91,
                 from /home/vsameer1/Downloads/FreeRTOS-Sim-master/Source/croutine.c:70:
/usr/include/features.h:367:25: fatal error: sys/cdefs.h: No such file or directory
compilation terminated.
Makefile:127: recipe for target 'obj/croutine.o' failed
make: *** [obj/croutine.o] Error 1

### Resolved by: 
Issue is resolved by installing the libraries as shown below: 
### sudo apt install gcc-multilib g++-multilib
