# 🧾 Git Cheat Sheet

## 🔧 Setup & Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global core.editor nano
git config --list
git init


## 📁 Repository Operations
git clone <repo-url>              # Clone a remote repo
git status                        # Show current status
git add <file>                    # Stage a file
git add .                         # Stage all files
git commit -m "message"           # Commit changes
git commit -am "message"          # Add and commit tracked files
git rm <file>                     # Remove a file
git mv <old> <new>                # Rename or move file


## 🔄 Branching & Merging
git branch                        # List branches
git branch <name>                 # Create new branch
git checkout <branch>             # Switch branch
git checkout -b <name>            # New + switch
git merge <branch>                # Merge into current
git rebase <branch>               # Reapply commits on top
git branch -d <branch>            # Delete a branch


## 🔁 Remote Repositories
git remote -v                     # Show remotes
git remote add origin <url>       # Add remote
git push origin <branch>          # Push to remote
git push -u origin <branch>       # Set upstream
git pull                          # Fetch + merge
git fetch                         # Only fetch
git remote rename <old> <new>     # Rename remote


## 🔍 History & Inspection
git log                           # Show commit history
git log --oneline                 # Compact log
git diff                          # Unstaged changes
git diff --staged                 # Staged changes
git show <commit>                 # Show commit details


## 💣 Undo & Reset
git reset <file>                  # Unstage a file
git reset --hard                  # Discard all changes
git checkout -- <file>            # Discard file changes
git revert <commit>               # Revert a commit
git reset --soft HEAD~1           # Undo commit, keep staged
git reset --mixed HEAD~1          # Undo commit, unstage


## 📦 Stashing & Cleaning
git stash                         # Stash changes
git stash apply                   # Apply stashed changes
git stash list                    # View stashes
git stash drop                    # Drop a stash
git clean -f                      # Delete untracked files
git clean -fd                     # Files + directories


## 🔖 Tagging
git tag                           # List tags
git tag <name>                    # Create tag
git tag -a <name> -m "msg"        # Annotated tag
git push origin <tag>             # Push single tag
git push origin --tags            # Push all tags


## 🛠️ Advanced
git cherry-pick <commit>          # Apply commit
git reflog                        # Show HEAD history
git bisect start                  # Begin binary search
git blame <file>                  # Who changed what