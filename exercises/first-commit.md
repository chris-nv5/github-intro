# Exercise: Your First Commit

Practice the basic Git workflow by adding a short learning note to this repository and proposing it to the group in a pull request. Plan for about 20 minutes.

## Before You Start

- Install [Git](https://git-scm.com/downloads) and sign in to [GitHub](https://github.com/).
- Ask a repository maintainer for collaborator access. If the group uses forks, fork this repository and clone your fork instead.
- Open a terminal in the folder where you keep projects.

Set the name and email Git should record on your commits. Use the email associated with your GitHub account if you want GitHub to attribute the commit to you.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Steps

1. On GitHub, copy the repository's clone URL. Clone it and enter the new folder:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create a branch for your work. Replace `your-name` with a short name using lowercase letters and hyphens:

   ```bash
   git switch -c exercise/your-name-first-commit
   ```

3. Copy [the learning log template](../notes/learning-log-template.md) to `notes/your-name.md`. Add your name and one thing you learned or one question you have. Keep the note suitable for sharing with the group.

4. Review the change, stage the note, and commit it:

   ```bash
   git status
   git diff
   git add notes/your-name.md
   git commit -m "Add my learning note"
   ```

5. Push your branch to GitHub:

   ```bash
   git push -u origin exercise/your-name-first-commit
   ```

6. On GitHub, open a pull request from your branch into `main`. Summarize what you added and include one question or learning takeaway. A teammate can use the [pull request template](../templates/pull-request-template.md) as a guide.

7. Read the review feedback, make any agreed updates on the same branch, and merge the pull request once it is approved.

## Check Your Work

- Your note is in `notes/` and contains no private information.
- Your commit is on a branch, not directly on `main`.
- Your pull request explains the change and is ready for a teammate to review.

If Git reports an error you don't recognize, run `git status` and ask the group before trying commands that discard changes.