# Chapter 2 - Navigation

The Linux operating system is organized in a tree of folders that contain other
folders or files. Usually "folders" are called "directories".

![](https://y.yarn.co/773a8c98-5f66-4ac7-92d8-805fa7049561_text.gif)


## Commands

| Command | Action                                      |
|---------|---------------------------------------------|
| pwd     | print working directory, where even am I rn |
| ls      | list, what is even in here                  |
| cd      | change directory, take me to...             |


## Shorthand

The `cd` command gives you some shorthand symbols so you don't have to type
everything out, all the time.

| Shorthand | Description        |
|-----------|--------------------|
| ~         | home directory     |
| -         | previous directory |
| .         | current directory  |
| ..        | parent directory   |
| /         | filesystem root    |


## Examples

| Command        | Action                                                       |
|----------------|--------------------------------------------------------------|
| cd ..          | go "up" one directory, to the current directory's parent     |
| cd -           | go to the directory you were just in                         |
| cd ~           | go to your Home directory                                    |
| cd /           | go to the root of the file system                            |
| cd ~/Downloads | go to your Downloads directory                               |
| ls -alh        | list all files (even hidden files) with human readable sizes |

When you use `cd -`, it takes you to whatever directory you were last in. That
"last directory" is stored in the environment variable "\$OLDPWD". So, if you
forget what your last directory was, you can recover it by typing `echo "$OLDPWD"`.


## Chapter 1 - Addendum

Jon mentioned `Ctrl-r` for using the `reverse-i-search` utility (or program).
I'm pretty sure "reverse-i-search" is short for "reverse interactive search".
Here's how to use it

  - press `Ctrl-r` to start the reverse-i-search utility
  - type in your search term
  - press `Ctrl-r` repeatedly to cycle through matches
  - press `Ctrl-o` to "open" that command in the terminal, without executing it
  - OR press enter to execute that command
  - OR press `Ctrl-g` to "get out" of the reverse-i-search utility

You can also just type `history` to see a list of your previous commands.

One particularly cool way to use `Ctrl-r` is to include a comment at the end
of your command to sort of "tag" it so that it is easier to find later. On the
command line, you can comment something with a hash sign, `#` and everything
after that symbol is completely ignored by the terminal.

### Mac

Mac actually uses a slightly different utility from `reverse-i-search` and it
is called `bck-i-search`. The main difference is that instead of using `Ctrl-o`
to "open" the command in the terminal without executing it, you press `Esc`
twice. Everything else works as above.