# Linux chgrp Command
-------------------
### Command Introduction (命令介绍)
> **chgrp - change group ownership**
### Command Format and Options (命令格式和选项)
```
#chgrp --help
Usage: chgrp [OPTION]... GROUP FILE...
  or:  chgrp [OPTION]... --reference=RFILE FILE...
Change the group of each FILE to GROUP.
With --reference, change the group of each FILE to that of RFILE.

  -c, --changes          like verbose but report only when a change is made
  -f, --silent, --quiet  suppress most error messages
  -v, --verbose          output a diagnostic for every file processed
      --dereference      affect the referent of each symbolic link (this is
                         the default), rather than the symbolic link itself
  -h, --no-dereference   affect symbolic links instead of any referenced file
                         (useful only on systems that can change the
                         ownership of a symlink)
      --no-preserve-root  do not treat '/' specially (the default)
      --preserve-root    fail to operate recursively on '/'
      --reference=RFILE  use RFILE's group rather than specifying a
                         GROUP value
  -R, --recursive        operate on files and directories recursively

The following options modify how a hierarchy is traversed when the -R
option is also specified.  If more than one is specified, only the final
one takes effect.

  -H                     if a command line argument is a symbolic link
                         to a directory, traverse it
  -L                     traverse every symbolic link to a directory
                         encountered
  -P                     do not traverse any symbolic links (default)

      --help     display this help and exit
      --version  output version information and exit

Examples:
  chgrp staff /u      Change the group of /u to "staff".
  chgrp -hR staff /u  Change the group of /u and subfiles to "staff".

GNU coreutils online help: <http://www.gnu.org/software/coreutils/>
For complete documentation, run: info coreutils 'chgrp invocation'
```
### Command Example (命令范例)
```

  chgrp

  Change group ownership of files and directories.

  - Change the owner group of a file/directory:
    chgrp group path/to/file_or_directory

  - Recursively change the owner group of a directory and its contents:
    chgrp -R group path/to/directory

  - Change the owner group of a symbolic link:
    chgrp -h group path/to/symlink

  - Change the owner group of a file/directory to match a reference file:
    chgrp --reference=path/to/reference_file path/to/file_or_directory


```
