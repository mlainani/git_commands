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

## Branches

- Create a remote branch

```
git push -u origin mlainani/teco_mcast_storm_1732980_take_two
```
