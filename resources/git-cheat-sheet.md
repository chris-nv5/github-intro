# Git Cheat Sheet

Quick reference for common Git commands.

## Getting Started

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git init                    # Create new repository
git clone <url>             # Clone existing repository
```

## Branches

```bash
git branch                  # List branches
git branch <branch-name>    # Create branch
git branch -d <branch-name> # Delete branch

git checkout <branch>       # Switch to branch
git switch <branch>         # Modern alternative (Git 2.23+)
git checkout -b <branch>    # Create and switch in one command
```

## Making Changes

```bash
git status                  # Check current status
git add <file>              # Stage file for commit
git add .                   # Stage all changes
git add *.js                # Stage by pattern

git commit -m "message"     # Commit with message
git commit -am "message"    # Stage tracked files and commit

git diff                    # Show unstaged changes
git diff --staged           # Show staged changes
git diff <branch1> <branch2> # Compare branches
```

## History & Logs

```bash
git log                     # Show commit history
git log --oneline           # Condensed log
git log -n 5                # Show last 5 commits
git log --author="Name"     # Filter by author
git log --since="2 weeks ago" # Filter by date
git log <file>              # History of specific file

git show <commit>           # Show commit details
git blame <file>            # Show who changed each line
```

## Undoing Changes

```bash
git restore <file>          # Discard changes in working directory
git restore --staged <file> # Unstage file
git revert <commit>         # Create new commit undoing changes
git reset HEAD~1            # Undo last commit (keep changes)
git reset --hard HEAD~1     # Undo last commit (discard changes)
```

## Remote & GitHub

```bash
git remote                  # List remotes
git remote -v               # List remotes with URLs
git remote add origin <url> # Add remote
git remote remove origin    # Remove remote

git fetch                   # Get updates from remote (no merge)
git pull                    # Fetch and merge from remote
git push                    # Push commits to remote
git push -u origin <branch> # Push branch and set upstream
git push origin <branch>    # Push to specific branch
```

## Merging & Rebasing

```bash
git merge <branch>          # Merge branch into current branch
git rebase <branch>         # Rebase current branch on top of another
git merge --abort           # Cancel ongoing merge
git rebase --abort          # Cancel ongoing rebase
```

## Stashing (Temporary Storage)

```bash
git stash                   # Save changes without committing
git stash list              # List stashed changes
git stash pop               # Apply and remove last stash
git stash apply             # Apply stash without removing
git stash drop              # Delete stash
```

## Tags & Releases

```bash
git tag                     # List tags
git tag <tag-name>          # Create lightweight tag
git tag -a <tag> -m "msg"   # Create annotated tag
git push origin <tag>       # Push specific tag
git push origin --tags      # Push all tags
```

## Useful Combinations

```bash
# Before submitting a PR
git fetch origin
git rebase origin/main
git push -u origin <branch>

# Clean up commits
git rebase -i HEAD~3        # Interactive rebase last 3 commits

# See what branch you're about to delete
git branch -vv              # Show branch with tracking info

# Undo the last push (careful!)
git revert HEAD
git push

# Get back accidentally deleted branch
git reflog                  # Show all past HEAD positions
```

## Common Workflows

### Feature Branch Workflow
```bash
git checkout -b feature/my-feature
# ... make changes ...
git add .
git commit -m "Add my feature"
git push -u origin feature/my-feature
# Create PR on GitHub
```

### Sync Fork with Upstream
```bash
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

### Squash Commits Before PR
```bash
git rebase -i HEAD~3        # Interactive mode for last 3 commits
# Change 'pick' to 'squash' for commits you want to combine
git push --force-with-lease
```

## Pro Tips

| Tip | Command |
|-----|---------|
| Create alias for long command | `git config --global alias.co checkout` |
| See visual branch graph | `git log --graph --oneline --all` |
| Find commit by message | `git log -S "text to find"` |
| Temporarily switch branches | `git stash` before switching |
| See what was just deleted | `git reflog` |
| Case-insensitive search | `git log -i --grep="case"` |

---

**Remember**: When in doubt, use `git status` to see where you are!
