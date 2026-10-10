# Project 1: Linux File and Directory Management

## 📌 Project Overview

This project demonstrates basic Linux file and directory management using commands on an Amazon Linux server. It covers creating, listing, copying, moving, renaming, and deleting files and directories.

## 🎯 Objectives

- Understand the Linux directory structure.
- Create and manage files and directories.
- Copy, move, and rename files.
- View file contents.
- Search for files and directories.
- Practice essential Linux commands.

## 🛠️ Environment

- Operating System: Amazon Linux
- Platform: AWS EC2
- Access: SSH Terminal
- Shell: Bash

## 1. Check the Current Directory

**Command:**

```bash
pwd
```

**Sample Output:**

```text
/root/project1-file-management
```

**Explanation:** Displays the current working directory.

## 2. List Files and Directories

**Command:**

```bash
ls
```

**Sample Output:**

```text
documents  reports  notes.txt
```

**Explanation:** Displays files and directories in the current location. Output varies depending on the files present.

## 3. Display Detailed File Information

**Command:**

```bash
ls -lah
```

**Sample Output:**

```text
total 12K
drwxr-xr-x  4 root root  80 Oct 10 10:00 .
drwxr-xr-x 10 root root 200 Oct 10 09:00 ..
drwxr-xr-x  2 root root  40 Oct 10 10:00 documents
drwxr-xr-x  2 root root  40 Oct 10 10:00 reports
-rw-r--r--  1 root root  25 Oct 10 10:00 notes.txt
```

**Explanation:** Displays hidden files, permissions, ownership, sizes, and timestamps. The output above is an example.

## 4. Create a Directory

**Command:**

```bash
mkdir practice
```

**Verify:**

```bash
ls -ld practice
```

**Sample Output:**

```text
drwxr-xr-x 2 root root 6 Oct 10 10:10 practice
```

**Explanation:** Creates a directory named `practice`.

## 5. Create Nested Directories

**Command:**

```bash
mkdir -p practice/documents/reports
```

**Verify:**

```bash
find practice -type d
```

**Sample Output:**

```text
practice
practice/documents
practice/documents/reports
```

**Explanation:** Creates multiple levels of directories in one command.

## 6. Create a File

**Command:**

```bash
touch practice/notes.txt
```

**Verify:**

```bash
ls -l practice/notes.txt
```

**Explanation:** Creates an empty file if it does not already exist.

## 7. Add Text to a File

**Command:**

```bash
echo "Linux file management practice" > practice/notes.txt
```

**Verify:**

```bash
cat practice/notes.txt
```

**Output:**

```text
Linux file management practice
```

**Explanation:** Writes text to a file. The `>` operator replaces existing content.

## 8. Append Text to a File

**Command:**

```bash
echo "Learning Linux commands on Amazon Linux" >> practice/notes.txt
```

**Verify:**

```bash
cat practice/notes.txt
```

**Output:**

```text
Linux file management practice
Learning Linux commands on Amazon Linux
```

**Explanation:** The `>>` operator appends text without replacing existing content.

## 9. Copy a File

**Command:**

```bash
cp practice/notes.txt practice/notes-backup.txt
```

**Verify:**

```bash
ls -l practice/
```

**Explanation:** Creates a copy of the file.

## 10. Copy a Directory

**Command:**

```bash
cp -r practice/documents practice/documents-backup
```

**Verify:**

```bash
ls -l practice/
```

**Explanation:** Copies a directory and its contents recursively.

## 11. Move a File

**Command:**

```bash
mkdir -p practice/archive
mv practice/notes-backup.txt practice/archive/
```

**Verify:**

```bash
ls -l practice/archive/
```

**Explanation:** Moves the file into the archive directory.

## 12. Rename a File

**Command:**

```bash
mv practice/notes.txt practice/linux-notes.txt
```

**Verify:**

```bash
ls -l practice/
```

**Explanation:** Renames a file using the `mv` command.

## 13. View File Contents

**Command:**

```bash
cat practice/linux-notes.txt
```

Other useful commands:

```bash
head -n 5 practice/linux-notes.txt
tail -n 5 practice/linux-notes.txt
less practice/linux-notes.txt
```

**Explanation:**
- `cat` displays the file contents.
- `head` displays the first lines.
- `tail` displays the last lines.
- `less` allows interactive viewing.

## 14. Find Files and Directories

**Command:**

```bash
find practice -type f
```

**Sample Output:**

```text
practice/linux-notes.txt
practice/archive/notes-backup.txt
```

Find a specific file:

```bash
find practice -type f -name "*.txt"
```

**Explanation:** Searches for files by name or file type.

## 15. Check File Type

**Command:**

```bash
file practice/linux-notes.txt
```

**Sample Output:**

```text
practice/linux-notes.txt: ASCII text
```

**Explanation:** Identifies the type of a file.

## 16. Check Disk Usage

**Command:**

```bash
du -sh practice
```

**Sample Output:**

```text
12K     practice
```

**Explanation:** Displays the total disk space used by the directory. Actual output may vary.

## 17. Remove a File

**Command:**

```bash
touch practice/temp.txt
rm practice/temp.txt
```

**Verify:**

```bash
ls practice/
```

**Explanation:** Deletes the specified file. Use `rm` carefully because deleted files may not be recoverable.

## 18. Remove an Empty Directory

**Command:**

```bash
mkdir practice/empty-folder
rmdir practice/empty-folder
```

**Explanation:** `rmdir` removes an empty directory.

## 19. Display the Directory Structure

**Command:**

```bash
find practice -print
```

**Explanation:** Displays the directory hierarchy and its contents.

## 20. Clean Up the Practice Environment

Run this only after completing the exercises:

```bash
rm -r practice
```

**Warning:** This permanently removes the `practice` directory and its contents. Confirm the path before running the command.

## 📚 Key Linux Commands Learned

| Command | Purpose |
|---|---|
| `pwd` | Display current directory |
| `ls -lah` | List files with details |
| `mkdir` | Create directories |
| `touch` | Create empty files |
| `cat` | Display file contents |
| `echo` | Write text |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `find` | Search files and directories |
| `file` | Identify file types |
| `du -sh` | Check directory disk usage |
| `rm` | Delete files |
| `rmdir` | Delete empty directories |

## ✅ Project Outcome

After completing this project, I gained practical experience with Linux file and directory management, file operations, directory navigation, and essential terminal commands using Amazon Linux.

## 👨‍💻 Technologies Used

- Linux
- Amazon Linux
- Bash Terminal
- AWS EC2
