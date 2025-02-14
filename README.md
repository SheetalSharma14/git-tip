# Git Tips

Use this handy git comments and guide to enhance your workflow. :) 

Inspired by: https://www.atlassian.com/git , https://learngitbranching.js.org/

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Git Configuration
| Command | Description |
| ------- | ----------- |
| `git config` | Congiure Username and Email used in code commit |
| `git config --list` | View your Git configuration |
| `git config --global user.name "Your Name"` | Congiure Username |

### Rename a Git Branch - Local
| Command | Description |
| ------- | ----------- |
| `git branch -m new-name` | If you are on the branch you want to rename, give new name |
| `git branch -m old-name new-name` | If you are on a different branch, give old name for the branch and the new one |

### Rename a Git Branch - Remote
### First do the same as rename a git branch - Local
| Command | Description |
| ------- | ----------- |
| `git push origin :old-name new-name` | Delete the remote branch with the old name and push the new branch to the remote repository |
| `git push origin -u new-name` | Reset the upstream branch for the new-name local branch |

### Find the Git Repository URL
| Command | Description |
| ------- | ----------- |
| `git config --get remote.origin.url` | gives Repository URL in a format similar to: git@github.com:<user>/<project>.git or ssh://git@github.com:<port>/<user>/<project>.git |


### Delete .git/index.lock file
| Command | Description |
| ------- | ----------- |
| `rm -f .git/index.lock` | deletes the existing index.lock file |
