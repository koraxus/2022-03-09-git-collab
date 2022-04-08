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

Changes to b1 commit 1
Changes to b1 commit 2
Changes to b2 commit 1
Changes to b2 commit 2

set up for rebase conflict

```
git checkout -b conflict_branch_1
echo "Changes to b1 commit 1" >> README.md
cat README.md
git commit -am "b1 c1"
echo "Changes to b1 commit 2" >> README.md
git commit -am "b1 c2"
git log --oneline --graph --all
git checkout main
git log --oneline --graph --all
git checkout -b conflict_branch_2
echo "Changes to b2 commit 1" >> README.md
git commit -am "b2 c1"
echo "Changes to b2 commit 2" >> README.md
git commit -am "b2 c2"
 ```

 - Branch protection rules force you to practice collaboration on your own
 - `git reset --hard <HASH>`: force move current branch to <HASH> location
 - `git log --oneline --graph --all`
