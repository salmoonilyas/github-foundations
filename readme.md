# GitHub Foundations (Data Camp Course)

**Course:** GitHub Foundations
**Provider:** Data Camp

Course Link: https://app.datacamp.com/learn/skill-tracks/github-foundations

---

1. Introduction to Git

---

## 1.1 Introduction to Git  
The benefits and fundamentals of Git for version control in software and data projects.

- Introduction to version control
    Version control allows track and change files in different states or changes overtime.
    List all files and sub-directories in the current folder: ls

- Navigating the shell  
    Get current working directory: pwd
    Move to another directory: cd <directory name>

- Checking the version of Git
    Checking git version: git --version

- Creating repos  
  Git repo is directory containing files and sub-directories, and Git Storage.

- Converting an existing project
    git init

- Creating a new repo  
    git init <project name>

- Staging and committing files  
    Add the file to PC, then add it to staging area by initializing, and then save it to git by using commit.

- Adding a file to the staging area  
    git add <file name>
    git add . :memo: **Note:** The "." adds all files, directories and subdirectories to the commit.

- Saving files
    git commit -m "Description of the commit"

---

## 1.2 Version history  
Covers how to compare files at different points in time, and restore files to their previous state.

- Viewing the version history  
    Git commit structure have three parts:
        1. Commit: Contains the metadata - author, log message, commit time.
        2. Tree: Tracks the names and locations of the files and directories in the repo.
                 like a directory - mapping keys to files/directories.
        3. Blob: Binary Large Object
                 may contain data of any kind
                 a compressed snapshot of a file's contents.

    Visualizing the commit structure:
    ![Visualizing the commit structure](.\images\1.2.commit-structure.png)

- Viewing a repository's history  
    git log :memo: **Note:** Shows the list of commit in chronological order.

- Finding the log message  
    git log :memo: **Note:** Shows commit name, Author, date and message.

- Version history tips and tricks  
    git show 227fa856 :memo: **Note:** Only need first 8-10 characters of the commit. The output displays the log entry for that commit at the top, followed by a diff output showing changes between the file in that commit and the current version in the repo. At the bottom, it shows the data.

![Git show [commit]](.\images\1.2.version-history.png)

- Limiting the view of a repo's history  
    git log -3 :memo: **Note:** Shows last three commits.

- Viewing a file's history  
    git log report.md :memo: **Note:**Filters commit by report name. 
    git log -2 report.md :memo: **Note:** Filter by report name and only show last two commits.

- Filtering commits by date  
   git log --since ="Month Day Year" --until ="Month Day Year" :memo: **Note:** Filter commits by date, the until part is optional.
    Acceptable filter date formats, could be in natural language format or in conventional date formats such as: git log --since "2 weeks ago".

- Comparing versions
    git diff :Difference between two versions.


    Summary
![alt text](images/1.2.git-diff-summary.png)

- Comparing staged files  
    git diff report.md :compare the last committed version of report with a modified version that is unstaged.
    ![alt text](images/1.2.version-history.png)
    The line in light blue font shows the comparison of what changed between the two versions. The minus 0 and 0 indicate that version A starts at line 0 and has 0 lines, and the plus 1 and 78 show that version B starts at line 1 and has 78 lines.

    git diff --staged report.md :compare the last committed version of report with a modified version that is in the staging area.
    git diff --staged :compare the last committed version of report with all staged files.

- Comparing to the second most recent commit
    git diff commit-id-B commit-id-A
    git diff HEAD~1 HEAD

- Restoring and reverting files  
    Used to resolve problems by restoring to previous version.

    git revert : reinstates the previous versions and makes a commit with older versions. Restores all files updated in the given commit.
    The git revert works on commits, not individual files.

    git checkout :To revert a single file
    git checkout HEAD~1 --report.md  :To unstage single file. Then commit the new file.

    git restore: To unstage a single file

    ![Summary of unstaging](images/1.2.git-revert-summary.png)

- Unstaging a file  
    git restore --staged summary_statistics.cvs
    git restore --staged :remove all files from the staging area

- Reverting a commit
    git revert HEAD : Restoring to last commit. Opens as text editor Save and exit using Crtl+O Enter Crtl +X.
    git revert --no-edit HEAD :avoid opening text editor
    git revert -n HEAD : Revert without committing (brings files to staging area) -n = no commit
    
---























1. Intermediate Git

2. Introduction to Github Concepts

Introduction to GitHub Products: A Complete Guide

4. Intermediate GitHub Concepts

Introduction to GitHub Codespaces
