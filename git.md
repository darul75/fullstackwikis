### Tuto

https://try.github.io/levels/1/challenges/1

### Working from a Fork

For dev use if coding from a fork.

All instructions here: https://help.github.com/articles/syncing-a-fork

```
git pull
git fetch upstream
git checkout master
git merge upstream/master
```

### Tagging

For release purpose, use of tags commands examples:

```
git tag 0.1.1 -m "0.1.1 release"
```
overriding existing tag

```
git tag -f -a v0.1.4 -m "memory"
```

push it

```
git push --tags
```

We may use it then from servers to fetch releases.

### Commit

Status
```
git status -s
```

Commit
```
git commit -m 'comment'
```

Rollback to last Repo Commit
```
git reset --hard origin/master
```

Directory content example

```
git add directory/*
```

### Icons

http://www.emoji-cheat-sheet.com/

### SSH Key

For Heroku or other, here command to register private key on device

ssh-add -K /path/of/private/key

### Heroku

- Download heroku toolbelt :
https://toolbelt.heroku.com/

- Run grunt from the src directory
- Install missing npm packages ( ie cordova )
- go to ../build/beedeez
- git commit
or
- git commit -am "mep 01082014"
- git push origin master
