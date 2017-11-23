# gitconfig
Configuración de git

## Global

### General

    git config --global ui.color auto
    git config --global user.name "Pepito Pérez"
    git config --global user.mail "pperez@mikasa.com"

### Alias

    git config --global alias.cl clone

    git config --global alias.st "status -sb"
    git config --global alias.last "log -1 --stat"
    git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %Cblue<%an>%Creset' --abbrev-commit --date=relative --all"
    git config --global alias.dc "diff --cached"

    git config --global alias.unstage "reset HEAD --"

    git config --global alias.ci commit
    git config --global alias.ca "commit -a"

    git config --global alias.ri "rebase -i"
    git config --global alias.ria "rebase -i --autosquash"
    git config --global alias.fix "commit --fixup"
    git config --global alias.squ "commit --squash"

    git config --global alias.cp cherry-pick
    git config --global alias.co checkout
    git config --global alias.br branch

## Por proyecto

    git config http.proxy "usernm:pass@ipProxy:port"

