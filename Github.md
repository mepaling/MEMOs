# Github

## For merging 

### master and A are 2 branches, and master has the newest code

master merge to A with no fast-forward then push to remote branch
``` Bash
git pull
git checkout A
git merge master --no-ff
git commit -m "merge master to A"
git push
```

### if conflict occurs you need to fix them by hand, then add those files again
``` Bash
git status
git add <file>
git commit -m "merge master to A"
git push
```