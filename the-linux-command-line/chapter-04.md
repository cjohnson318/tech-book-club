# Chapter 4 - Manipulating File and Directories

![](https://media.tenor.com/04KdcsfRodUAAAAd/conspiracy-charlie-day.gif)

## Copying and Moving Things Around

The MVP commands of this chapter are:
  - `cp` - copy
  - `mv` - move
  - `mkdir` - make directory
  - `rm` - remove

I think the big takeaway from this chapter are the options that make some of
these commands more useful and sometimes less destructive:
  - `-i`, `--interactive`, asks for confirmation before overwriting a file
  - `-r`, `--recursive`, do task recursively
  - `-u`, `--update`, skip files that don't need to be moved/copied

Use `-i`. Accidentally overwriting files is a horrifying.

One thing that isn't mentioned is that `mkdir` does not allow you to create one
directory inside another directory without a `-p` option, which I assume is 
short for path. So, to be clear, the following will not work:

    mkdir new-dir/nested-dir

But this *will* work

    mkdir -p new-dir/nested-dir

## Links

Think of files as having two parts, a name part and a data part. The name part
holds the file's name, and the data part holds the file's contents. When we
create new hard links, we are actually creating new name parts that point to
the same data part.

Symbolic links were created after hard links, and they can do two things that
hard links cannot:
  1. Symbolic links can span across physical devices
  2. Symbolic links can reference directories, in addition to files

When we create a symbolic link, we are creating a text description of where the
target file is relative to the symbolic link.