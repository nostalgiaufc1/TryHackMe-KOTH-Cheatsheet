# TryHackMe KOTH Cheatsheet

If you're looking for root permissions

`find / -type f \( -perm -4000 -o -perm -2000 \) -print`


**using chattr**

**you can keep you're name in this file**

`chattr +i /root/king.txt`

fixing the vulnerability in /etc/sudoers - Below is an exmaple 
`# User privilege specification
root ALL=(ALL=ALL) ALL
teste ALL=(root) SETENV:NOPASSWD: /usr/bin/git *, /usr/bin/chattr
test1 ALL=(root) NOPASSWD: /bin/su test1, /usr/bin/chattr`

**full tty shell*

`python3 -c 'import pty; pty.spawn("/bin/sh")'
export TERM=xterm
Ctrl + z
stty raw -echo;fg`


**Using find** 

- you can use the command `find` to look for flags (Below is an example)
`find / -name flag.txt 2>/dev/null
find / -name user.txt 2>/dev/null
find / -name .flag 2>/dev/null
find / -name flag 2>/dev/null
find / -name root.txt 2>/dev/null`

**How to check who's logged into the system?**

- to kill someone's session just use the following command.
`pkill -9 -t pts/1`
just put the pts of the user you want from the machine.

**Changed ssh user password**
if you want to change user password just enter the following command 
``passwd [UserName]``





**CREDITS - MatheuZ Security**
Credits - TryHackMe KOTH

my discord is nostalgia#3903 


