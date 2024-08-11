
# Notes I made from Git and GitHub Crash Course - taught by Kunal Kushwaha.

## Basic Git Commands

### Initializing and Checking Status

- `git init`: Initialize Git in a folder.
- `git status`: Show the status of files (untracked, modified, staged).

### Listing Files

- `ls`: List files in a directory.
- `ls -a`: Show hidden files, including the `.git` folder.
- `ls .git`: Show contents of the `.git` folder.

### Adding and Committing Changes

- `git add .`: Stage all new and modified files.
- `git add <filename>`: Stage a specific file.
- `git commit -m "Your message"`: Commit staged changes with a descriptive message.

### Viewing History

- `git log`: Display the commit history.

### Undoing Changes

- `git restore --staged <filename>`: Unstage a file while keeping changes.
- `git reset <commit-hash>`: Reset to a specific commit (use with caution).

### Branching

- `git branch <branch-name>`: Create a new branch.
- `git checkout <branch-name>`: Switch to a different branch.
- `git merge <branch-name>`: Merge a branch into the current branch.

## Working with Remote Repositories

### Setting Up Remotes

- `git remote add origin <url>`: Link a local repository to a GitHub repo.
- `git remote -v`: View all remote repositories linked to the current folder.
- `git remote remove origin`: Remove the 'origin' remote.
- `git remote set-url origin <url>`: Update the URL of the 'origin' remote.

### Pushing and Pulling

- `git push origin <branch-name>`: Push local changes to a remote branch.
- `git push origin <branch-name> -f`: Force push when local changes aren't reflected online (use with caution).
- `git pull origin <branch-name>`: Fetch and merge changes from a remote branch.

### Cloning and Forking

- `git clone <url>`: Download a repository to your local machine.
- Fork (via GitHub UI): Create a personal copy of someone else's project.

## Advanced Git Features

### Stashing

- `git stash`: Temporarily store modified, tracked files.
- `git stash pop`: Apply stored stash content and remove it.
- `git stash clear`: Remove all stashed entries.

### Rebasing

- `git rebase -i <commit-hash>`: Interactively rebase commits (useful for squashing).

### Working with Forks

- `git remote add upstream <url>`: Add the original repository as a remote named 'upstream'.
- `git fetch --all --prune`: Fetch all updates from all remotes and remove deleted references.
- `git reset --hard upstream/main`: Reset your local main branch to match the upstream main.
- `git pull upstream main`: Alternative to fetch and reset, pulls changes from the upstream main branch.

## Useful Terminal Commands

- `ls`: List files in a directory.
- `ls -a`: Show hidden files.
- `touch <filename>`: Create a new file.
- `rm -rf <filename>`: Delete a file or directory (use with caution).
- `cat <filename>`: Display the contents of a file.

## Vim Basic Commands

Vim is a powerful text editor often used with Git for commit messages:

- `vi <filename>`: Open a file in Vim.
- `i`: Enter insert mode.
- `Esc`: Exit insert mode.
- `Esc` + `:` + `w` + `q`: Save and quit (`:wq`).
- `Esc` + `Shift` + `z` + `z`: Alternative way to save and quit (`ZZ`).
- `Esc` + `:` + `q` + `!`: Quit without saving (`:q!`).
- `Esc` + `:` + `x`: Save and quit (shorthand for `:wq`).

## Best Practices

1. Write clear, concise commit messages.
2. Create a new branch for each feature or bug fix.
3. Regularly pull changes from the upstream repository to stay updated.
4. Use meaningful branch names that describe the work being done.
5. Review your changes before committing.

## Handling Merge Conflicts

Merge conflicts occur when Git can't automatically resolve differences in code between two commits. To resolve:

1. Open the conflicting file(s) and locate the conflict markers.
2. Edit the file to resolve the conflict.
3. Remove the conflict markers.
4. Stage the resolved files.
5. Commit the changes.

Remember to test your code after resolving conflicts to ensure everything works correctly.

## Working with Pull Requests

- One branch typically corresponds to one pull request.
- Different branches (features) can lead to different pull requests.
- Use "Fetch upstream" on GitHub to get the current version of the forked main project.
- Merging a pull request incorporates changes from your forked project into the main project.

## Squashing Commits

To combine multiple commits into one:

1. Use `git rebase -i <commit-hash>` to start an interactive rebase.
2. In the editor, change `pick` to `s` (squash) for the commits you want to combine.
3. Save and close the editor.
4. Edit the combined commit message in the next editor screen.
   
------
