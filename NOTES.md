#### Test a syscall
1. Create a user file in "user/<newfile>.c"
1. Add `$U/_<newfile>` to Makefile.
1. Run `make fs.img`
1. Start up the system with `make qemu-gdb` and you should see your new program. 

#### Add a syscall
TODO but look through:
* usys.pl
* syscall.c
* syscall.h
* user.h

And the pattern seems to be
* Implement in sysproc.c
* Implement in proc.c

where sysproc.c is an interface to calling proc.c

#### How to debug
