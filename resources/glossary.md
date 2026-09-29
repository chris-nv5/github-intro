# GitHub & Git Glossary

Essential terms and definitions for GitHub and Git.

---

## A

**Author**  
The person who originally wrote the code in a commit. (Different from Committer)

**Upstream**  
The original repository you forked from. Referenced as `upstream/branch-name`.

---

## B

**Base Branch**  
The target branch for a pull request (usually `main` or `develop`).

**Blame** (Git Blame)  
A tool showing which author changed each line of a file and when.

**Branch**  
A parallel version of your code. Allows independent development without affecting main code.

**Branch Protection**  
Rules that prevent direct pushes to a branch (e.g., require PR review before merging).

---

## C

**Clone**  
Create a local copy of a remote repository on your computer.

**Commit**  
A snapshot of your repository at a specific point in time. Includes changes, author, timestamp, and message.

**Commit Message**  
Descriptive text accompanying a commit explaining what changed and why.

**Compare**  
GitHub feature showing differences between two branches or commits.

**Conflict** (Merge Conflict)  
When changes in two branches contradict each other and can't be automatically merged.

---

## D

**Default Branch**  
The main branch created when you initialize a repository (usually `main`).

**Diff**  
A display of differences between two versions of a file. Green = added, Red = removed.

**Distributed Version Control**  
System where every developer has a complete copy of the repository history.

---

## F

**Fetch**  
Download updates from remote without merging. Shows you what changed but doesn't modify your files.

**Fork**  
Create your own copy of someone else's repository. Used for contributing to open source.

**Forking Workflow**  
Development pattern where contributors fork, create PRs, and the maintainer merges changes.

---

## G

**Git**  
Open-source version control system that tracks changes to code.

**GitHub**  
Web-based hosting service for Git repositories with collaboration features.

---

## H

**HEAD**  
Pointer indicating your current branch and commit position.

---

## I

**Issue**  
GitHub's way of tracking bugs, features, and tasks. Central to project management.

**Issue Template**  
Pre-written format for issues to ensure consistent information (e.g., bug, feature request).

---

## L

**Label**  
Tags added to issues and PRs for organization (e.g., `bug`, `documentation`, `urgent`).

**Local Repository**  
The copy of a repository on your computer.

---

## M

**Main/Master**  
The primary/default branch representing the production-ready code.

**Merge**  
Combine changes from one branch into another.

**Merge Commit**  
A commit created when merging branches, connecting two separate histories.

**Milestone**  
A grouping of issues and PRs used for release planning (e.g., "v1.0").

---

## O

**Origin**  
Default name for the remote repository you cloned from.

**Open Source**  
Software with publicly available source code that anyone can view, modify, and distribute.

---

## P

**Pull**  
Fetch updates and automatically merge them into your current branch.

**Pull Request (PR)**  
Formal proposal to merge changes from one branch to another. Allows for review and discussion.

**Push**  
Send your local commits to a remote repository.

---

## R

**Rebase**  
Reapply commits from one branch on top of another. Alternative to merge.

**Remote**  
A version of your repository hosted on a server (e.g., GitHub).

**Repository**  
A project folder containing all files, history, and Git metadata.

**Revert**  
Create a new commit that undoes changes from a previous commit.

---

## S

**Stash**  
Temporarily save changes without committing them.

**Status**  
Current state of your repository (modified files, staged changes, current branch).

---

## T

**Tag**  
A label for a specific commit, often used for releases (e.g., `v1.0.0`).

**Team**  
Group of GitHub users organized within an organization for permission management.

---

## U

**Upstream Branch**  
The remote branch your local branch is tracking (e.g., `origin/main`).

**User**  
Individual GitHub account.

---

## V

**Version Control**  
System for tracking and managing changes to files over time.

---

## W

**Workflow**  
Standardized process for how a team uses branches, PRs, and merges (e.g., GitHub Flow, Git Flow).

---

## Additional Concepts

### Git Flow
Branching model with multiple permanent branches:
- `main` - Production releases
- `develop` - Integration branch
- Feature branches from `develop`
- Release and hotfix branches

### GitHub Flow
Simpler model with one permanent branch:
- `main` - Always deployable
- Feature branches from `main`
- PR review and test
- Merge and deploy immediately

### Common Abbreviations
- **VCS** - Version Control System
- **PR** - Pull Request
- **CI/CD** - Continuous Integration / Continuous Deployment
- **LOC** - Lines of Code
- **SSH** - Secure Shell (for authentication)
- **HTTPS** - Secure HTTP (for cloning/pushing)
- **API** - Application Programming Interface

---

**Don't remember a term?** Check back here or ask in [GitHub Discussions](../../discussions)!
