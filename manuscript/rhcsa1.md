# Understand and use essential tools

## Access a shell prompt and issue commands with correct syntax

To access a shell prompt once the system has finished booting: `Ctrl`+`Alt`+`F2`

## Use input-output redirection (>, >>, |, 2>, etc.)

### Input redirection from files

Execute `command` using `file` as the source of input:

    <command> < <file>

### Output redirection to files

I> ## Note
I>
I> Remember that `>>` can be used in place of `>` to append to the destination file instead of overwriting it.

Execute `command` and redirect **STDOUT** to `file`:

    <command> > <file>

Execute `command` and redirect **STDERR** to `file`:

    <command> 2> <file>

Execute `command` and redirect both **STDOUT** and **STDERR** to `file`:

    <command> &> <file>

### Piping

Execute `command1` and redirect **STDOUT** to `command2`:

    <command1> | <command2>

Execute `command1` and redirect both **STDOUT** and **STDERR** to `command2`:

    <command1> 2>&1 | <command2>

## Use grep and regular expressions to analyze text

    grep [options] <regexp> <file>

## Access remote systems using ssh

    ssh [options] [user@]<host>[:port]

## Log in and switch users in multiuser targets

    su - <user>

## Archive, compress, unpack, and uncompress files using tar, star, gzip, and bzip2

I> ## Note
I>
I> For the following examples, `tar` and `star` are interchangeable.

Archive and compress using (s)tar/gzip:

    tar cvzf <file>.tgz <directory>

Uncompress and unpack using (s)tar/gzip:

    tar xvzf <file>.tgz

Archive and compress using (s)tar/bzip:

    tar cvjf <file>.tbz <directory>

Uncompress and unpack using (s)tar/bzip:

    tar xvjf <file>.tbz

## Create and edit text files

    nano <file>

## Create, delete, copy, and move files and directories

Create a file:

    nano <file>

Delete a file:

    rm <file>

Copy a file from `src` to `dst`:

    cp <src> <dst>

Move (rename) a file from `src` to `dst`:

    mv <src> <dst>

Create a directory:

    mkdir <dir>

Delete a directory:

    rm -r[f] <dir>

Copy a directory from `src` to `dst`:

    cp -r <src> <dst>

Move (rename) a directory from `src` to `dst`:

    mv <src> <dst>

## Create hard and soft links

Create a hard link:

    ln <target> <link>

Create a soft link `link` that points to `target`: 

    ln -s <target> <link>

## List, set, and change standard ugo/rwx permissions

List permissions:

    ll [file]

Change permissions:

    chmod <mode> <file>

## Locate, read, and use system documentation including man, info, and files in /usr/share/doc

Try command line help:

    <command> --help

Access man pages:

    man [section] <page>

Additional documentation can often be found in `/usr/share/doc`:

    less /usr/share/doc/<path>
