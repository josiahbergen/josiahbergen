```assembly
section .data
  text db  "https://jojobinx.com/a/", 0xa

section .text
  global _start

_start:
  mov rax, 1
  mov rdi, 1 
  mov rsi, text
  mov rdx, 24
  syscall

  mov rax, 60
  mov rdi, 0
  syscall
```

```bash 
$ nasm -f elf64 -o hello.o hello.asm
$ ld hello.o -s -o hello
$ ./hello
https://jojobinx.com/a/
$ ▂
```

<!---
Jojobinx17/Jojobinx17 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
