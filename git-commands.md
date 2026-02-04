# 📚 Git Commands Cheat Sheet

A comprehensive guide to Git commands for version control.

---

## 🚀 Getting Started

### Configuration
```bash
# Set your username
git config --global user.name "Your Name"

# Set your email
git config --global user.email "your.email@example.com"

# Check your configuration
git config --list

# Set default branch name
git config --global init.defaultBranch main
```

### Initialize & Clone
```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone <repository-url>

# Clone a specific branch
git clone -b <branch-name> <repository-url>
```

---

## 📝 Basic Commands

### Status & Changes
```bash
# Check the status of your working directory
git status

# Show changes between working directory and staging area
git diff

# Show changes between staging area and last commit
git diff --staged
```

### Staging & Committing
```bash
# Stage a specific file
git add <filename>

# Stage all changes
git add .

# Stage all changes (including deletions)
git add -A

# Commit with a message
git commit -m "Your commit message"

# Stage and commit in one step
git commit -am "Your commit message"

# Amend the last commit
git commit --amend -m "New commit message"
```

---

## 🌳 Branching

### Branch Management
```bash
# List all local branches
git branch

# List all branches (local and remote)
git branch -a

# Create a new branch
git branch <branch-name>

# Switch to a branch
git checkout <branch-name>

# Create and switch to a new branch
git checkout -b <branch-name>

# Delete a local branch
git branch -d <branch-name>

# Force delete a local branch
git branch -D <branch-name>

# Rename current branch
git branch -m <new-name>
```

### Merging
```bash
# Merge a branch into current branch
git merge <branch-name>

# Merge with no fast-forward
git merge --no-ff <branch-name>

# Abort a merge
git merge --abort
```

---

## 🔄 Remote Operations

### Remote Management
```bash
# List remotes
git remote -v

# Add a remote
git remote add origin <repository-url>

# Remove a remote
git remote remove <remote-name>

# Change remote URL
git remote set-url origin <new-url>
```

### Push & Pull
```bash
# Push to remote
git push origin <branch-name>

# Push and set upstream
git push -u origin <branch-name>

# Force push (use with caution!)
git push --force

# Pull from remote
git pull origin <branch-name>

# Fetch without merging
git fetch origin
```

---

## 📜 History & Logs

```bash
# View commit history
git log

# View history in one line format
git log --oneline

# View history with graph
git log --oneline --graph --all

# View last n commits
git log -n 5

# View changes in a specific commit
git show <commit-hash>

# View who changed each line
git blame <filename>
```

---

## ↩️ Undoing Changes

```bash
# Discard changes in working directory
git checkout -- <filename>

# Unstage a file
git reset HEAD <filename>

# Reset to a previous commit (keep changes staged)
git reset --soft <commit-hash>

# Reset to a previous commit (keep changes unstaged)
git reset --mixed <commit-hash>

# Reset to a previous commit (discard all changes)
git reset --hard <commit-hash>

# Revert a commit (creates new commit)
git revert <commit-hash>
```

---

## 🏷️ Tags

```bash
# List all tags
git tag

# Create a lightweight tag
git tag <tag-name>

# Create an annotated tag
git tag -a <tag-name> -m "Tag message"

# Push a tag to remote
git push origin <tag-name>

# Push all tags
git push origin --tags

# Delete a local tag
git tag -d <tag-name>
```

---

## 📦 Stashing

```bash
# Stash current changes
git stash

# Stash with a message
git stash save "Your stash message"

# List all stashes
git stash list

# Apply the latest stash
git stash apply

# Apply and remove the latest stash
git stash pop

# Apply a specific stash
git stash apply stash@{n}

# Drop a stash
git stash drop stash@{n}

# Clear all stashes
git stash clear
```

---

## 🔍 Searching

```bash
# Search for a string in tracked files
git grep "search-term"

# Search commit messages
git log --grep="search-term"

# Find commits that changed a file
git log --follow <filename>
```

---

## 🛠️ Advanced Commands

### Rebasing
```bash
# Rebase current branch onto another
git rebase <branch-name>

# Interactive rebase for last n commits
git rebase -i HEAD~n

# Continue after resolving conflicts
git rebase --continue

# Abort rebase
git rebase --abort
```

### Cherry-Pick
```bash
# Apply a specific commit to current branch
git cherry-pick <commit-hash>

# Cherry-pick without committing
git cherry-pick -n <commit-hash>
```

### Clean
```bash
# Preview files to be removed
git clean -n

# Remove untracked files
git clean -f

# Remove untracked files and directories
git clean -fd
```

---

## 💡 Pro Tips

1. **Always pull before push** to avoid conflicts
2. **Write meaningful commit messages** following conventional commits
3. **Use branches** for new features and bug fixes
4. **Never force push** to shared branches
5. **Use `.gitignore`** to exclude unnecessary files

---

## 📖 Useful Aliases

Add these to your `.gitconfig`:
```bash
[alias]
    st = status
    co = checkout
    br = branch
    ci = commit
    lg = log --oneline --graph --all
    last = log -1 HEAD
    unstage = reset HEAD --
```

---

*Happy Coding! 🎉*
