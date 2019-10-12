# Git Daily Usage Quick Reference

## Manual
```
man git
```

## Config Git
```
git config --global push.default simple
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

## Quick References
- `git init` - Create a Git repository in the current folder.
- `git status` - View the status of each file in a repository.
- `git add .` - Stage files
- `git commit` - Commit the staged files with a descriptive message.
- `git log` - View a repository’s commit history.

## Branch Management
- `git branch` - list all branches
- `git show-branch` - Show branches and their commits

## New branch
```
git checkout -b new-branch-name
git push --set-upstream origin new-branch-name
```

## Changes not staged for commit
```
git add <file>          # Update what will be committed
git checkout -- <file>  # Discard changes
```

## Change back to previous version
Rewriting the most recent commit message
```
git checkout origin/master <fileName>  # checkout the original version from master branch
git add .                              # stage the changes
git commit --amend                     # If you don't specify a commit message with -m, you will be prompted with the previous commit message as default
git push -f
git log --stat                         # to see your amended commit with the extra changes
```

## Rebase commits in PR
```
git fetch origin            # Updates origin/master
git rebase origin/master    # Rebases current branch onto origin/master
```
resolve Conflict in text editor and then
```
git add .
git rebase --continue
```
push the rebased commit to branch
```
git push -f origin your_local_branch
```
Multiple commits rebase to single commit
```
git rebase -i HEAD~2    # number of commits
git push -f origin your_local_branch
```

Abort the rebase - make sure you `stash` or `commit` any uncommited changes first or you will lose them irrevocably
```
git rebase --abort
```

## Reset commits
```
git reset --hard origin/master
```
will remove all commits not in `origin/master` where `origin` is the repo name and `master` is the name of the branch

```
git reset --hard <SOME-COMMIT>
```
will make your current branch back to point at `<SOME-COMMIT>` and then make the files in your working tree and the index ("staging area") the same as the versions committed in `<SOME-COMMIT>`

## Git clean
```
git clean -xdf
```

## Github repo change remote URL
```
git remote -v
git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git
git remote set-url origin https://github.com/USERNAME/OTHERREPOSITORY.git
```

## Check logs
```
git log --oneline
```

## Git Tag
```
git tag <tagname> -a "Description"
git push origin <tagname>
```
