## Advanced Git Topics
Notes from Conquering Git: Advanced training Guide (Video) - https://github.com/ignazioc

### Git Stashing
- Simple stash/pop examples
- Stash and tracked/indexed Files
- Managed multiple stahses
- Stashed into a branch

#### Stash and Pop
- Stashing our changes
```
git stash  # equal to git stash save
```
- Re-applying our changes with pop
```
# save the most recent changes, work like stack
git stash pop
```

#### Tracked Indexed Files
```
git stash --keep-index
git stash --include-untracked
```

#### Multiple Stashes
```
git stash
git stash save "change message"
git stash save "another message"
git stash list
# which will return
stash@{0}: change message
stash@{1}: another message
git stash apply 1 # to apply changes
```

#### Stahing into a Branch
```
git stash save -k -u #check k / u mmeaning
git stash branch new_branch
```

### Branching under the Hood
#### Branching Basic
- Creating a branch
- Changing current branch
- Resetting a branch to a specific commit

#### HEAD and Other Names
#### Branches on filesystem
#### Git Branch Advanced Tricks - rename, track, contains

### Git Merging under the Hood
