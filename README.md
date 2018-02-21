# gitconfig
Configuración de git

## Global

### General

    git config --global ui.color auto
    git config --global user.name "Pepito Pérez"
    git config --global user.email "pperez@mikasa.com"

### Alias

    git config --global alias.cl clone

    git config --global alias.st "status -sb"
    git config --global alias.last "log -1 --stat"
    git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %Cblue<%an>%Creset' --abbrev-commit --date=relative --all"
    git config --global alias.dc "diff --cached"
    # git config --global alias.ds "diff --staged"
    git config --global alias.dh "diff HEAD"
    git config --global alias.dp "diff --word-diff --unified=10"
    git config --global alias.so "show --pretty='parent %Cred%p%Creset commit %Cred%h%Creset%C(yellow)%d%Creset%n%n%w(72,2,2)%s%n%n%w(72,0,0)%C(cyan)%an%Creset %Cgreen%ar%Creset'"

    git config --global alias.unstage "reset HEAD --"

    git config --global alias.ci commit
    git config --global alias.ca "commit -a"
    git config --global alias.cam "commit --all --message"

    git config --global alias.ri "rebase -i"
    git config --global alias.ria "rebase -i --autosquash"
    git config --global alias.fix "commit --fixup"
    git config --global alias.squ "commit --squash"

    git config --global alias.cp cherry-pick
    git config --global alias.co checkout
    git config --global alias.br branch
    git config --global alias.qm '!git checkout $1; git merge @{-1}'

## Por proyecto

    git config http.proxy "http://usernm:pass@ipProxy:port"
