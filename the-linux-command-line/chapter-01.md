# Chapter 01 - What Is The Shell

This chapter is pretty light, it covers

  - opening a shell
  - typing commands
  - using the up/down arrows to recover previous commands
  - using the left/right arrows to move the cursor for editing
  - using the command `exit` to quit the shell

Having an `exit` command when you can just click an (X) button to close a 
window sounds dumb, but it's useful when you use one shell to log into another
shell on another computer across the country. Once you're in that remote shell,
how do you get back out? Use `exit`, and it'll pop you back into your original
shell where you started from. More on that later.

Practically speaking, you'll never really need to know the difference between 
"shell" and "terminal emulator".


## Windows

After you type `wsl` into PowerShell or CMD to get yourself into the Windows 
Subsystem for Linux, then you can use `exit` to get yourself back
to PowerShell/CMD. If WSL is not installed, you need to run `wsl --install` in 
the PowerShell terminal, and then restart the machine.[^1]


## Mac

The `free` command won't be recognized on your shell, but you can use `vm_stat` 
to get similar information in a different format. The term "pages"
refers to the smallest unit of memory usable by the system. In the case of
Apple M1 silicon, this is 16KB. The field "Pages free" are the number of 16KB
units of memory that are free.[^2]


[^1]: [Install Linux on Windows with WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
[^2]: [Is there a Mac OS X Terminal version of the "free" command in Linux systems?](https://apple.stackexchange.com/questions/4286/)
