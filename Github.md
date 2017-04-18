# Github

## For merging 

_master and A are 2 branches, and master has the newest code_

First, master merge to A with no fast-forward then push to remote branch
``` Bash
git pull
git checkout A
git merge master --no-ff
git commit -m "merge master to A"
git push
```

__if conflict occurs you need to fix them by hand, then add those files again__
``` Bash
git status
git add <file>
git commit -m "merge master to A"
git push
```

## For creating new orphan branch
First create the orphan branch "orphan_branch_name" on local
```Bash
git checkout --orphan orphan_branch_name
```
Untrack everything from git
```Bash
git rm --cached -r .
```
Delete everything from folder
```Bash
rm -rf .
```
add README and .gitignore by hand
```Bash
vim README.md 
vim .gitignore
```
Track README and .gitignore
```Bash
git add README.md
git add .gitignore
```
__Commit and push__
```Bash
git commit -m "create orphan branch orphan_branch_name"
git push -u pseudo pseudo
```
