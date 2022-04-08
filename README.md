# 2022-03-09-git-collab

- `git clone <URL>`: "downloads" the repository to the current directory
	- `git init`: creates a git repo locally

- `git branch <NAME>`: creates <NAME> where HEAD is
	- `git branch -a`: list all your branches
- `git switch <NAME>`: switch to branch <NAME>
	- `git checkout <NAME>`: "older" way to switch branches
  - shortcut: `git switch -c <NAME>`: create and move in 1 step
  - `git checkout -b <name>`: older way to create and move
  - The PR will updat if you push new changes 

- Cleaning up after PR merge
	- Delete the branch on the remote
	- `git fetch --prune`: update the local history
	- `git branch -d <NAME>`: delete the branch <NAME>
		- Note: lower-case d (use -D for force delete)

