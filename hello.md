========================================
       BASIC GIT COMMANDS CHEATSHEET
========================================

1. CONFIGURATION
----------------
Set your name and email (used in commit history):
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"

Check configuration:
  git config --list


2. INITIALIZING & CLONING
-------------------------
Initialize a new local Git repository:
  git init

Clone an existing remote repository:
  git clone <repository-url>


3. BASIC WORKFLOW (STAGING & COMMITTING)
----------------------------------------
Check the status of your working directory and staging area:
  git status

Stage a specific file for the next commit:
  git add <filename>

Stage all changes in the current directory:
  git add .

Commit staged changes with a descriptive message:
  git commit -m "Commit message"

Commit all tracked, modified files directly (skipping 'git add'):
  git commit -am "Commit message"


4. VIEWING HISTORY & CHANGES
----------------------------
View commit history:
  git log

View condensed one-line commit history:
  git log --oneline

View graphical branch history:
  git log --oneline --graph --all

Show unstaged changes compared to the last commit:
  git diff

Show staged changes:
  git diff --staged

Show details of a specific commit:
  git show <commit-hash>


5. BRANCHING & MERGING
----------------------
List all local branches:
  git branch

Create a new branch:
  git branch <branch-name>

Switch to an existing branch:
  git switch <branch-name>
  # or: git checkout <branch-name>

Create and switch to a new branch:
  git switch -c <branch-name>
  # or: git checkout -b <branch-name>

Merge a branch into the current branch:
  git merge <branch-name>

Delete a branch (safely):
  git branch -d <branch-name>


6. REMOTE REPOSITORIES
----------------------
List connected remotes:
  git remote -v

Add a new remote repository:
  git remote add origin <repository-url>

Fetch updates from remote without merging:
  git fetch

Pull changes from remote and merge into current branch:
  git pull origin <branch-name>

Push local commits to remote repository:
  git push origin <branch-name>

Push and set upstream tracking branch (first push):
  git push -u origin <branch-name>


7. UNDOING CHANGES
------------------
Discard changes in a file (restore working tree):
  git restore <filename>

Unstage a file while keeping its changes:
  git restore --staged <filename>

Revert a commit by creating a new commit with opposite changes:
  git revert <commit-hash>

Reset to a specific commit (keeps changes in working directory):
  git reset <commit-hash>

Reset everything strictly to a commit (discards all uncommitted changes):
  git reset --hard <commit-hash>


8. STASHING (TEMPORARY WORK)
----------------------------
Save uncommitted changes temporarily:
  git stash

List all stashes:
  git stash list

Restore and remove the most recent stash:
  git stash pop

Discard the most recent stash:
  git stash drop

