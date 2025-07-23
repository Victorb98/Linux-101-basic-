**❤️‍🔥 Linux-101-Basics: Diving Deep into the OS for Cyber Defenders! 🕵️‍♂️**

🚀 TryHackMe Linux 101: My First Steps into Cybersecurity Command Mastery! 💻🔒

This repository documents fundamental Linux commands and file system navigation learned through the TryHackMe platform. It serves as a quick reference and a log of my initial steps into the Linux command line.

## Table of Contents

* [Objective](#objective)
* [Environment](#environment)
* [Screenshot](#screenshot)
* [Commands and Outputs](#commands-and-outputs)
    * [`ls` - List Directory Contents](#1-ls---list-directory-contents)
    * [`whoami` - Display Current Username](#2-whoami---display-current-username)
    * [`pwd` - Print Working Directory](#3-pwd---print-working-directory)
    * [`ls -l` - Long Listing Format](#4-ls--l---long-listing-format)
    * [`cd` - Change Directory](#5-cd---change-directory)
    * [`cat` - Concatenate and Display File Content](#6-cat---concatenate-and-display-file-content)
    * [`touch` - Create Empty Files](#7-touch---create-empty-files)
    * [`mkdir` - Make Directories](#8-mkdir---make-directories)
    * [`rm` - Remove Files or Directories](#9-rm---remove-files-or-directories)
    * [`ls -a` - List All Files (Including Hidden)](#10-ls--a---list-all-files-including-hidden)

---

## Objective

The primary objective was to familiarize myself with essential Linux commands for navigating the file system, managing files and directories, and understanding basic file properties.

## Environment

All commands were executed within a remote Linux terminal provided by the TryHackMe platform.

## Screenshot

Here's a screenshot of the terminal session demonstrating the commands and their outputs:

![TryHackMe Linux 101 Session](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/images/TRYHACKME_LINUX_101.PNG?raw=true)


<img width="1366" height="728" alt="TRYHACKME LINUX 101" src="https://github.com/user-attachments/assets/4f7e27f1-cd17-4484-9019-90da3c29aa5b" />



## Commands and Outputs

Below is a detailed breakdown of each command executed, its output, and a brief explanation of its function.

### 1. `ls` - List Directory Contents

Lists files and directories within the current working directory.

```bash
tryhackme@linux1:~$ ls
access.log  folder1  folder2  folder3  folder4  newfolder  testfolder
planation: Shows all visible files and subdirectories present in the current location.

2. whoami - Display Current Username
Identifies the current user logged into the system.

Bash

tryhackme@linux1:~$ whoami
tryhackme
Explanation: Confirms that the active user is tryhackme.

3. pwd - Print Working Directory
Displays the full path of the current working directory.

Bash

tryhackme@linux1:~$ pwd
/home/tryhackme
Explanation: Indicates that the current directory is /home/tryhackme.

4. ls -l - Long Listing Format
Provides a detailed list of files and directories, including permissions, number of links, owner, group, size, and last modification date/time.

Bash

tryhackme@linux1:~$ ls -l
total 88
-rw-rw-r-- 1 tryhackme tryhackme  65522 May 10  2021 access.log
drwxr-xr-x 2 tryhackme tryhackme   4096 May 10  2021 folder1
drwxr-xr-x 2 tryhackme tryhackme   4096 May 10  2021 folder2
drwxr-xr-x 2 tryhackme tryhackme   4096 May 10  2021 folder3
drwxr-xr-x 2 tryhackme tryhackme   4096 May 10  2021 folder4
drwxrwxr-x 2 tryhackme tryhackme   4096 Jul 23 20:24 newfolder
drwxrwxr-x 2 tryhackme tryhackme   4096 Jul 23 20:31 testfolder
Explanation:

-rw-rw-r--: File permissions (owner read/write, group read/write, others read). A d at the start indicates a directory.

1: Number of hard links.

tryhackme tryhackme: Owner username and group name.

65522 / 4096: Size in bytes.

May 10 2021 / Jul 23 20:xx: Last modification date and time.

5. cd - Change Directory
Used to navigate into a specified directory.

Bash

tryhackme@linux1:~$ cd folder4
tryhackme@linux1:~/folder4$ ls
note.txt
Explanation:

cd folder4: Changes the current working directory to folder4.

ls: Lists the contents of folder4, showing note.txt.

6. cat - Concatenate and Display File Content
Displays the content of a file. (Note: Attempting to cat a directory will result in an error).

Bash

tryhackme@linux1:~/folder4$ cat folder4
cat: folder4: Is a directory
Explanation: The command failed because cat is used for files, and folder4 is a directory. The intention might have been to cat note.txt.

7. touch - Create Empty Files
Creates a new, empty file or updates the timestamp of an existing file.

Bash

tryhackme@linux1:~/folder4$ touch test_test.txt
Explanation: Creates an empty file named test_test.txt within the folder4 directory.

8. mkdir - Make Directories
Used to create new directories.

Bash

tryhackme@linux1:~/folder4$ mkdir new_test
Explanation: Creates a new directory named new_test inside folder4.

9. rm - Remove Files or Directories
Deletes files or directories. Use with caution!

Bash

tryhackme@linux1:~/folder4$ rm test.txt
Explanation: Removes the file test.txt from the folder4 directory. (This assumes test.txt existed or was created prior to test_test.txt).

10. ls -a - List All Files (Including Hidden)
Displays all files and directories, including those that start with a dot (.), which are hidden by default.

Bash

tryhackme@linux1:~/folder4$ ls -a
.  ..  .cache  .Xauthority  access.log  .bash_history  .bash_logout  .bashrc  .profile  folder1  folder2  folder3  folder4  newfolder  testfolder
Explanation:

.: Represents the current directory.

..: Represents the parent directory.

Other dot files (.cache, .bash_history, etc.) are system or user-specific configuration files that are typically hidden.
