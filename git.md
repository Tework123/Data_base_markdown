![git.png](..%2F..%2F%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F%2Fgit.png)


## Work with last commit

Rewrite last commit message:

    git commit --amend

If you need change files in commit. You must create simple commit with --amend.
Last bad commit change on this. 

Delete file from index:

    git restore --staged <name_file>
    git rm --cached <name_file>


Return start state commit(delete changes): 

    git reset --hard HEAD


Delete certain commit:

    git reset --hard HEAD~1

## Merge, cherry-pick, rebase, revert

Merge

    git merge branch_with_new_func

Подтягивает не всю ветку, как мердж или ребейз, а только до нужного коммита
    
    git cherry-pick 992cbbe

Rebase

    git rebase branch_with_new_func


Return from last commit and create new commit from them:

    git revert -m 1 HEAD


## Git tags and realise

Create on last commit, but you might attach them to any commit:

    git tag -a v3.0 -m "New release for v3.0"

Push tags to remote:

    git push --tags

## Useful commands:

Statistics add string in project:

    git log --stat

History of commits:

    git log --oneline --decorate --graph --all