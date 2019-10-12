## Closing github issues using keywords
The following keywords followed by an issue number will close the issue:
`close closes closed fix fixes fixed resolve resolves resolved #[issueNum]`

## Github SSH

## Github Changing a remote's URL
[Changing a remote's URL](https://help.github.com/articles/changing-a-remote-s-url/)
```
$ git remote -v
```
Switching remote URLs from HTTPS to SSH
```
$ git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git
```
Switching remote URLs from SSH to HTTPS
```
$ git remote set-url origin https://github.com/USERNAME/OTHERREPOSITORY.git
```
