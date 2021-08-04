# Introduction

Why git and github?
- Maintain and track history of projects.
- Code sharing and collaboration.

[Download](http://git-scm.com/) git.

## 1. Command lines

- `ls`: list
  - `-a`: all
- `mkdir`: make directory
- `cd`: change directory
- `touch`: create new file
- `cat`: display file contents
- `rm -rf`: delete file   

## 2. Basics

- Initialise a repo? `git init`
- Where is history stored? .git folder.
- Track changes: `git status`
  - Untracked? `git add .'`
  - Permanently save? `git commit -m "message"` here `-m ""` provide message
  - History log? `git log`
- Accidently deleted and commited?
  - `git reset 'hash from log'`: commits after hash code will be reset.
  - Previous commits? unsatged area (`git status`)
  - Don't want to loose recent cahnges but also not commit it? `git stash`: move to back stage!
    - Bring back to unstaged area? `git stash pop`
    - Remove them? `git stash clear`

## 3. New Repository

- Create one form github dashboard.
- Attach to my local project? `git remote add origin url` origin is url name.
- Check all the URLs attached to my folder? `git remote -v`

- Share changes: `git push url branch` like `git push origin master`

## 4. Branches

- Directed acyclic graph. now 'main' previously 'master'.
- Why? 
  - Working on new feature? create new branch.
- Never commit unfinalised changes on main branch.
- Create branch: `git branch name`
- **HEAD** from log shows the currently active branch!
- `git checkout name` and commit and add changes to this branch parallely.
- Merge to main code? `git merge name`

## 5. Working with existing projects in github

How to contribute?
- Create a copy of project into my own account: fork
- Work on it? `git clone url` origin url is from my personal account!
- Original project url is upstream url (froked): `git remote add upstream url`

- Add changes!
  - Make a changes.
  - Make a new branch.
  - Checkout to bring **Head** to new branch.
  - Add and commit.

- Merge to main project!
  - Request a 'pull request' and get reviewed.
  - Create different branch hence new pull requests for different features we are working on.
  - If a commit is removed using `reset` online repository has commits which local repository doesn't: force push it `git push origin name -f` since commits are interlinked.

- How to keep in sync with the main branch? **manually**
  - Fetch all the changes/commits: `git fetch --all --prune` i.e. `--all` branches and `--prune` deleted ones.
  - Reset main branch of my origin to that of upstream: `git reset --hard upstream/main`
  
- We can do all this from dashborad too!!

- Merging multiple commits into single commit: `git rebase -i hash`; pick or squash (`s`) to above commits.

