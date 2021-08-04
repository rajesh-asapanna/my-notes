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
