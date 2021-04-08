# My Git cheat sheet

## GitHub

- Get authentication prompt when pushing

```
git config --local credential.helper ""
```

## Commits

- Find branches the commit is on

```
git branch --contains d6f5ebbc3a5209f88bb2496cb3687a2999da4a23
* mlainani/teco_mcast_storm_1732980_take_two

git branch --contains 047d6e5084767a2972f7da5b325213987354888b
  ctopoc/tepco2019_pmr_nic
  develop
  mlainani/teco_mcast_storm_1732980
* mlainani/teco_mcast_storm_1732980_take_two
```

- Fix the author in last commit message

```
git commit --amend --author="Madani Lainani <madani.lainani@itron.com>"
```

- Replace last commit on remote branch

```
git push --force
```

## Branches

- Create a remote branch

```
git push -u origin mlainani/teco_mcast_storm_1732980_take_two
```

## ADS

```
mlainani@mustang:~/deleteme/IOTR-FW$ git push origin --delete foobar
To https://itron.visualstudio.com/RnD/_git/IOTR-FW
 - [deleted]         foobar

mlainani@mustang:~/deleteme/IOTR-FW$ git status
On branch foobar
Your branch is based on 'origin/foobar', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean

mlainani@mustang:~/deleteme/IOTR-FW$ git branch --unset-upstream

mlainani@mustang:~/deleteme/IOTR-FW$ git status
On branch foobar
nothing to commit, working tree clean

mlainani@mustang:~/deleteme/IOTR-FW$ git branch
* foobar
  master

mlainani@mustang:~/deleteme/IOTR-FW$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

mlainani@mustang:~/deleteme/IOTR-FW$ git branch -d foobar
error: The branch 'foobar' is not fully merged.
If you are sure you want to delete it, run 'git branch -D foobar'.
mlainani@mustang:~/deleteme/IOTR-FW$ git branch -D foobar
Deleted branch foobar (was a73f8df).

mlainani@mustang:~/deleteme/IOTR-FW$ git branch --all
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
```

kong@skullisland:~$ emacs ~/.gitconfig
kong@skullisland:~$ git config --global --unset-all user.name
kong@skullisland:~$ git config --global --unset-all user.
user.email   user.mail
kong@skullisland:~$ git config --global --unset-all user.email
kong@skullisland:~$ git config --global --unset-all user.mail
kong@skullisland:~$ git config --global --list



ADD REMOTE BRANCH


kong@skullisland:~/IOTR-FW$ git push --set-upstream origin test_branch
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.95 KiB | 667.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: Storing packfile... done (70 ms)
remote: Storing index... done (70 ms)
To vs-ssh.visualstudio.com:v3/itron/RnD/IOTR-FW
 * [new branch]      test_branch -> test_branch
Branch 'test_branch' set up to track remote branch 'test_branch' from 'origin'.



