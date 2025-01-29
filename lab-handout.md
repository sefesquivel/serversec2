# ServerSec2 Lab: Linux File Search and System Navigation

## Introduction
In this lab, you will learn and practice various Linux commands for locating files, searching through system directories, and finding specific content within files. These skills are essential for system administrators and security professionals.

## Objectives
- Master different file location commands in Linux
- Learn to use various find command options
- Practice combining search commands with grep
- Understand system file organization

## Prerequisites
- Basic knowledge of Linux command line
- Access to a Linux system with sudo privileges
- Basic understanding of file permissions

## Lab Environment Setup
1. Ensure you have access to the lab environment
2. The checker program will be available at your disposal
3. Run `sudo updatedb` before starting the lab to update the locate database

## Tasks and Scoring

### Basic File Location Commands (15 points)
1. **Using locate to display password locations** (5 points)
   - Use the locate command to find password-related files
   - Command format: `locate <filename>`
   - Hint: Update the database first using `sudo updatedb`

2. **Using whereis with multiple flags** (5 points)
   - Practice using whereis command with both -m and -u flags
   - Command format: `whereis -m -u <command>`
   - Focus on locating bash-related files

3. **Finding Command Path** (5 points)
   - Use which command to find exact command locations
   - Command format: `which <command>`
   - Focus on finding the ls command location

### Advanced File Finding (34 points)
4. **Basic Find Command** (5 points)
   - Learn to use find with the -name option
   - Command format: `find <starting_path> -name <filename>`
   - Practice finding the Downloads directory

5. **Find with AND Condition** (8 points)
   - Combine find conditions using -a
   - Command format: `find <starting_path> -user <username> -a -name <filename>`

6. **Find with OR Condition** (8 points)
   - Combine find conditions using -o
   - Command format: `find <starting_path> -user <username> -o -name <filename>`

7. **Finding Newer Files** (8 points)
   - Use find to compare file timestamps
   - Command format: `find <starting_path> -newer <reference_file>`

8. **Case-Insensitive Search** (5 points)
   - Practice case-insensitive file search
   - Command format: `find <starting_path> -iname <filename>`

### Time and Size Based Searches (32 points)
9. **Find by Modification Time (Days)** (8 points)
   - Search files by modification time in days
   - Command format: `find <starting_path> -mtime <n>`

10. **Find Recent Files (Minutes)** (8 points)
    - Search files by modification time in minutes
    - Command format: `find <starting_path> -mmin <n>`

11. **Size-based Search** (8 points)
    - Find files based on their size
    - Command format: `find <starting_path> -size <+/-size><unit>`

12. **No-owner Files Search** (8 points)
    - Locate files without valid owners
    - Command format: `find <starting_path> -nouser`

### Directory and Empty File Operations (19 points)
13. **Finding Empty Files** (7 points)
    - Locate empty files and directories
    - Command format: `find <starting_path> -empty`

14. **Directory-only Search** (5 points)
    - Find only directories
    - Command format: `find <starting_path> -type d`

15. **Depth-Limited Search** (7 points)
    - Practice limiting search depth
    - Command format: `find . -maxdepth 1`

### Advanced Content Search (30 points)
16. **Performance Data Search** (10 points)
    - Combine find with grep to locate CPU usage data
    - Command format: `find . -name numbers.txt -exec grep 'CPU Usage' {} \;`

17. **CSV Management Position Search** (10 points)
    - Search for manager positions in CSV files
    - Command format: `locate people.csv -exec grep 'Manager' {} \;`

18. **Engineering Staff Search** (10 points)
    - Find engineering department staff
    - Command format: `locate people.csv -exec grep 'Engineering' {} \;`

## Using the Checker Program
- To check a specific task: `./checker.py <task_number> <your_command>`
- To view progress: `./checker.py progress`
- To see hints: `./checker.py hints`
- To list all tasks: `./checker.py`

## Grading
- Total possible points: 130
- Each task has specific point values as listed above
- Points are awarded only for correct completion
- Multiple attempts are allowed

## Tips for Success
1. Read the task descriptions carefully
2. Use the hint system when stuck
3. Pay attention to command syntax and spacing
4. Test your commands before submitting
5. Use the man pages for detailed command information

## Submission
Your progress is automatically tracked by the checker program. Use the progress command to verify all tasks are completed before the lab deadline.

Good luck!