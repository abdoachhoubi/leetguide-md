# C Piscine - Shell 00

This is the first day of the shell piscine. The goal of this day is to learn the basics of the shell.

in order to do that, we have to do a lot of exercices.

## Exercices

### 00 - Print Groups

This exercice is about printing the groups of the user.

To do that, we have to use the command `groups` with the option `-l` to print the groups in a comma separated list.

```bash
groups -l $FT_USER | tr ' ' ','
```

### 01 - Print Users

This exercice is about printing the users of the group `staff`.

To do that, we have to use the command `grep` with the option `-E` to use a regex and the option `-o` to print only the matching part.

```bash
grep -Eo '^[^:]+:' /etc/group | tr -d ':'
```

### 02 - Hello

This exercice is about printing `Hello $FT_USER` where `$FT_USER` is the user's login.

To do that, we have to use the command `echo` with the option `-n` to not print a newline.

```bash
echo -n "Hello $FT_USER"
```

### 03 - Print Directory

This exercice is about printing the current directory.

To do that, we have to use the command `pwd` with the option `-P` to print the physical directory.

```bash
pwd -P
```

### 04 - List Files

This exercice is about listing all the files in the current directory.

To do that, we have to use the command `ls` with the option `-m` to print the names as a comma separated list.

```bash
ls -m -p -a
```

### 05 - List More Files

This exercice is about listing all the files in the current directory, including the hidden ones, with the user and group IDs.

To do that, we have to use the command `ls` with the option `-l` to print the long format, the option `-a` to print the hidden files and the option `-n` to print the user and group IDs.

```bash
ls -l -a -n
```

### 06 - Copy Files

This exercice is about copying the file `myfile` to `myfile_copy`.

To do that, we have to use the command `cp` with the option `-p` to preserve the file's attributes.

```bash
cp -p myfile myfile_copy
```

### 07 - Move Files

This exercice is about moving the file `myfile` to `myfile_copy`.

To do that, we have to use the command `mv` with the option `-f` to force the move.

```bash
mv -f myfile myfile_copy
```

### 08 - Delete Files

This exercice is about deleting the file `myfile`.

To do that, we have to use the command `rm` with the option `-f` to force the deletion.

```bash
rm -f myfile
```

### 09 - Create Directories

This exercice is about creating the directory `mydir`.

To do that, we have to use the command `mkdir` with the option `-p` to create the parent directories if they don't exist.

```bash
mkdir -p mydir
```

### 10 - Delete Directories

This exercice is about deleting the directory `mydir`.

To do that, we have to use the command `rm` with the option `-rf` to force the deletion.

```bash
rm -rf mydir
```

### 11 - Back to the Future

This exercice is about going to the parent directory of the current directory.

To do that, we have to use the command `cd` with the option `..` to go to the parent directory.

```bash
cd ..
```

### 12 - Lists

This exercice is about listing all the files in the current directory, including the hidden ones, with the user and group IDs, separated by commas, with the directories ending with a slash.

To do that, we have to use the command `ls` with the option `-m` to print the names as a comma separated list, the option `-p` to print a slash after the directories, the option `-a` to print the hidden files and the option `-n` to print the user and group IDs.

```bash
ls -m -p -a -n
```

### 13 - File Type

This exercice is about printing the type of the file `iamafile`.

To do that, we have to use the command `file` with the option `-b` to print only the type.

```bash
file -b iamafile
```

### 14 - We are Symbolic

This exercice is about creating a symbolic link to the file `ls` named `__ls__`.

To do that, we have to use the command `ln` with the option `-s` to create a symbolic link.

```bash
ln -s ls __ls__
```

### 15 - Copying a File

This exercice is about copying all the files in the current directory that end with `.sh` to the directory `backup`.

To do that, we have to use the command `cp` with the option `-p` to preserve the file's attributes and the option `-r` to copy the directories recursively.

```bash
cp -p -r *.sh backup
```
