# A git flow introduction

## Ordniary flow

When everything works really good

### Clone a repository

```
git clone https://github.com/klauszhang/git-flow
```

### Checkout to a new branch

```
git checkout -b my-branch
```

while repace _my-branch_ to your branch name

### Commit your change

I personally using a GUI tool to performe this step.
If not, please try

```
git add .
git commit -m "message add here"
```

### Push to remote

```
git push
```

## Avoid conflicts

- Working on different things/files/features
- Create PR ASAP, so that other people know what you're working on
- Small commits, small changes will make resolving conflicts much easier

### How to resolve conflicts

**TALK TO OTHER PEOPLE FIRST TO UNDERSTAND WHAT THEY DID**
There's two ways to resolve conflicts
`git merge`
`git rebase`

#### Git merge

- Will include other people's change into your branch, but looks clean on Github

### Git rebase

- Will make your git log nice and clean, but it is really hard to carry out when there's a big PR
- Have to do `git push -f`

## Collaborate

### A demo of using PR to manage multiple people work on the same target

- Create a base branch by `git checkout -b feature1`
- Push to remote and create a PR target to `master`
- For each collaborator, create their sub-branch by:
  - checkout to `feature1` branch first
  - checkout to a new branch by `git checkout -b feature1-sub1`
  - push to remote and create a PR, target to `feature1`
- Work on each branch and get each PR reviewed and merged
- After all the work have been done, merge main branch into `master`

### Update from master

- Click on update button on PR on `feature1` PR
- Click on update button on PR on each sub feature PR

### Confict resolution

**TALK TO OTHER PEOPLE FIRST TO UNDERSTAND WHAT THEY DID**

Start to resolve conflicts via your favourite tools

## Useful git tools

### git stash

This will allow to save your current WIP into a safe place so that you can use them in future, especially useful when you're working on multiple branches.

### git cherry-pick

This will allow you to pick the commit from other branches, useful to recover work from other branches

### git log

Useful to see what's the current status of work.
