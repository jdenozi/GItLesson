# GItLesson

## Install git and create a Github account
	The first two things you'll want to do are install git and create a free GitHub account.
## Clone the project 

### Linux based OS

For Linux, you need to configure the local GIT client with a username and email address,

    ``
    $ git config --global user.name "your_github_username"
    $ git config --global user.email "your_github_email"
    $ git config -l
    ```

Once GIT is configured, we can begin using it to access GitHub. Example:
    ```
    $ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
    > Cloning into `YOUR-REPOSITORY`...
    Username: <type your username>
    Password: <type your password or personal access token (GitHub)
    ```

Linux/Debian (Clone as follows):

    git clone https://<tokenhere>@github.com/<user>/<repo>.git

## Git config

```
[user]
	name = jdenozi
	email = j-denozi@outlook.com
[core]
    whitespace = cr-at-eol
	editor = vim

[color]
        ui = auto
[diff]
        tool = meld

[merge]
        tool = diffuse

[sendemail]
        smtpserver = smtp.orange.com

[alias]
    l = log --pretty=oneline
    ll = log --pretty=format:'%cs %H %s'
    spf = show --pretty=fuller
    sno = show --name-only
    lol = log --graph --decorate --pretty=oneline --abbrev-commit
    lola = log --graph --decorate --pretty=oneline --abbrev-commit --all
    ls = ls-files
    m = mergetool
    s = status
    who = shortlog -sne
    diffc = diff --cached
    changes = diff --name-status
    diffstat = diff --stat
    ca = commit --amend
    b = branch -av
    bl = branch -v
    r = remote -v
    c = checkout
    cb = checkout -b
    cp = cherry-pick
    cpa = cherry-pick --abort
    cpc = cherry-pick --continue
    rc = rebase --continue
    ra = rebase --abort
    sl = stash list
    rh = reset HEAD
    both-merged = !git-both-merged
    not-merged = !git-not-merged
    already-merged = !git-already-merged
    crom = checkout remotes/origin/master
    rirom = rebase -i remotes/origin/master
    po = push origin
    pohm = push origin HEAD:master
    pfohm = push -f origin HEAD:master
    pot = push origin --tags
    plo = pull origin
    tags = show-ref --tags 
    anw = !git diff -U0 -w --no-color -- \"$@\" | git apply --cached --ignore-whitespace --unidiff-zero "#"
    csm = commit -s -m
    a = add -u
    ai = add -u -i
    rbih = "!f() {\
        git rebase -i HEAD~$1; \
        }; f"
[format]
        signoff = true
[gc]
    auto = 0

[push]
    default = simple

[branch]
    autosetupmerge = always
```
