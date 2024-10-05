Here's a comprehensive list of Git commands grouped by category. These commands cover most use cases in Git, from setting up repositories to advanced Git operations like branching, merging, and debugging.
Basic Git Commands
1.	Initialize a Git repository
bash
Copy code
git init
2.	Clone a repository
bash
Copy code
git clone <repository_url>
3.	Check the status of the repository
bash
Copy code
git status
4.	Stage (add) files for commit
bash
Copy code
git add <file_or_directory>
# Add all changes
git add .
5.	Commit changes
bash
Copy code
git commit -m "commit message"
6.	View commit history
bash
Copy code
git log
Branching and Merging
1.	Create a new branch
bash
Copy code
git branch <branch_name>
2.	Switch to another branch
bash
Copy code
git checkout <branch_name>
3.	Create and switch to a new branch in one command
bash
Copy code
git checkout -b <branch_name>
4.	Merge a branch into the current branch
bash
Copy code
git merge <branch_name>
5.	Delete a branch
bash
Copy code
git branch -d <branch_name>
6.	Rename a branch
bash
Copy code
git branch -m <new_branch_name>
Remote Repositories
1.	Add a remote repository
bash
Copy code
git remote add origin <repository_url>
2.	View the remote repositories
bash
Copy code
git remote -v
3.	Push changes to a remote repository
bash
Copy code
git push origin <branch_name>
4.	Push changes and set upstream branch
bash
Copy code
git push -u origin <branch_name>
5.	Fetch updates from a remote repository
bash
Copy code
git fetch
6.	Pull updates from a remote repository (fetch + merge)
bash
Copy code
git pull
7.	Remove a remote repository
bash
Copy code
git remote remove origin
Stashing
1.	Stash changes (save work in progress)
bash
Copy code
git stash
2.	List stashed changes
bash
Copy code
git stash list
3.	Apply stashed changes
bash
Copy code
git stash apply
4.	Apply and delete the stash
bash
Copy code
git stash pop
5.	Drop a specific stash
bash
Copy code
git stash drop <stash@{n}>
Undoing Changes
1.	Unstage a file (but keep changes)
bash
Copy code
git reset <file>
2.	Undo the last commit (keep changes staged)
bash
Copy code
git reset --soft HEAD~1
3.	Undo the last commit (keep changes but unstaged)
bash
Copy code
git reset --mixed HEAD~1
4.	Undo the last commit and discard changes
bash
Copy code
git reset --hard HEAD~1
5.	Revert a specific commit (create a new commit that undoes the changes)
bash
Copy code
git revert <commit_hash>
6.	Discard changes in the working directory (to last commit)
bash
Copy code
git checkout -- <file>
Tagging
1.	Create a new tag
bash
Copy code
git tag <tag_name>
2.	List all tags
bash
Copy code
git tag
3.	Push a specific tag to the remote
bash
Copy code
git push origin <tag_name>
4.	Delete a tag locally
bash
Copy code
git tag -d <tag_name>
5.	Delete a tag from a remote
bash
Copy code
git push origin --delete <tag_name>
Collaboration and Tracking
1.	Show commits by a specific author
bash
Copy code
git log --author="<author_name>"
2.	Show a summary of changes
bash
Copy code
git log --stat
3.	Show changes introduced by each commit
bash
Copy code
git log -p
4.	Show the difference between two commits
bash
Copy code
git diff <commit1> <commit2>
5.	Show what branch you are currently on
bash
Copy code
git branch
6.	Show the commit history in one line
bash
Copy code
git log --oneline
Rebasing
1.	Rebase the current branch on another branch
bash
Copy code
git rebase <branch_name>
2.	Continue rebase after conflict resolution
bash
Copy code
git rebase --continue
3.	Abort a rebase
bash
Copy code
git rebase --abort
Cherry-Picking
1.	Cherry-pick a specific commit
bash
Copy code
git cherry-pick <commit_hash>
Submodules
1.	Add a Git submodule
bash
Copy code
git submodule add <repository_url>
2.	Initialize and update submodules
bash
Copy code
git submodule update --init --recursive
3.	Remove a Git submodule
bash
Copy code
git submodule deinit -f <submodule_path>
git rm -f <submodule_path>
rm -rf .git/modules/<submodule_path>
Configuration and Setup
1.	Set global username
bash
Copy code
git config --global user.name "Your Name"
2.	Set global email
bash
Copy code
git config --global user.email "your_email@example.com"
3.	Show current configuration
bash
Copy code
git config --list
4.	Set up Git to use an SSH key
bash
Copy code
git config --global core.sshCommand "ssh -i ~/.ssh/id_rsa"
5.	Set global editor
bash
Copy code
git config --global core.editor "vim"
________________________________________
Common Aliases
1.	Create a Git alias
bash
Copy code
git config --global alias.<alias_name> '<git_command>'
2.	Example: Create a shorthand for git status
bash
Copy code
git config --global alias.st 'status'
________________________________________
Advanced Commands
1.	Show a file from a previous commit
bash
Copy code
git show <commit_hash>:<file_path>
2.	Squash commits (interactive rebase)
bash
Copy code
git rebase -i <commit_hash>
3.	Fix the last commit message
bash
Copy code
git commit --amend -m "new message"
4.	Check which branch contains a commit
bash
Copy code
git branch --contains <commit_hash>
5.	Find out who changed what in a file (blame)
bash
Copy code
git blame <file>
This covers a wide range of Git commands, from basic to advanced operations. Let me know if you need more details on any of these commands!
4o
You said:
consolidated list and brief info below of each commands
ChatGPT said:
ChatGPT
Here’s a consolidated list of essential Git commands with brief descriptions for each:
Basic Commands
1.	git init
Initializes a new Git repository in the current directory.
2.	git clone <repo_url>
Clones a remote repository to your local machine.
3.	git status
Displays the state of the working directory and staging area (files changed, staged, etc.).
4.	git add <file>
Stages file(s) for commit, telling Git to track these changes.
5.	git commit -m "message"
Records changes in the repository with a commit message describing the changes.
6.	git log
Shows commit history with details about each commit.
Branching & Merging
1.	git branch <branch_name>
Creates a new branch.
2.	git checkout <branch_name>
Switches to the specified branch.
3.	git checkout -b <branch_name>
Creates and switches to a new branch in one step.
4.	git merge <branch_name>
Merges the specified branch into the current branch.
5.	git branch -d <branch_name>
Deletes a local branch.
Remote Repositories
1.	git remote add origin <repo_url>
Adds a remote repository called origin with the given URL.
2.	git push origin <branch_name>
Pushes changes to the remote repository on the specified branch.
3.	git pull
Fetches and merges changes from the remote repository into your current branch.
4.	git fetch
Fetches changes from the remote repository without merging.
5.	git remote -v
Shows the remote repositories and their URLs.
Stashing
1.	git stash
Temporarily saves changes that haven’t been committed, to clean the working directory.
2.	git stash apply
Applies stashed changes back to the working directory.
3.	git stash pop
Applies stashed changes and removes them from the stash list.
Undoing Changes
1.	git reset <file>
Unstages a file, but keeps its changes in the working directory.
2.	git reset --soft HEAD~1
Undoes the last commit but keeps the changes staged.
3.	git reset --hard HEAD~1
Undoes the last commit and discards all changes.
4.	git revert <commit_hash>
Creates a new commit that undoes the changes from a specific commit.
5.	git checkout -- <file>
Discards changes in the working directory, reverting to the last committed state.
Tagging
1.	git tag <tag_name>
Creates a new tag (a reference to a specific point in the commit history).
2.	git push origin <tag_name>
Pushes the specified tag to the remote repository.
3.	git tag -d <tag_name>
Deletes a tag locally.
Rebasing
1.	git rebase <branch_name>
Reapplies commits on top of another branch.
2.	git rebase --abort
Aborts the current rebase and returns to the previous state.
3.	git rebase --continue
Continues a rebase after resolving conflicts.
Cherry-Picking
1.	git cherry-pick <commit_hash>
Applies the changes from a specific commit to the current branch.
Submodules
1.	git submodule add <repo_url>
Adds a Git submodule, linking to another repository inside the current repo.
2.	git submodule update --init --recursive
Initializes, fetches, and updates all submodules.
Configuration
1.	git config --global user.name "Your Name"
Sets the global Git username.
2.	git config --global user.email "your_email@example.com"
Sets the global Git email.
3.	git config --list
Lists all the configuration settings.
Miscellaneous
1.	git log --oneline
Shows the commit history in a single line per commit.
2.	git blame <file>
Shows who changed each line in the file.
3.	git show <commit_hash>
Displays detailed information about a specific commit.
4.	git stash list
Lists all stashed changes.

