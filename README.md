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


# Trucos

## diff

    git config --global core.pager  'less -RFX'

    git diff --word-diff
    git diff --word-diff --unified=10               # dp diff prose
    git diff --patience                             # agrupa cambios
    git diff --histogram

    git config --global diff.algorithm histogram


## show

    git show head

    git show head~2

    git show head --pretty='parent %Cred%p%Creset commit %Cred%h%Creset%C(yellow)%d%Creset%n%n%w(72,2,2)%s%n%n%w(72,0,0)%C(cyan)%an%Creset %Cgreen%ar%Creset'

    git config --global alias.so "show --pretty='parent %Cred%p%Creset commit %Cred%h%Creset%C(yellow)%d%Creset%n%n%w(72,2,2)%s%n%n%w(72,0,0)%C(cyan)%an%Creset %Cgreen%ar%Creset'"

    git show head --no-patch

    git show head --stat

    git cat-file -p head            # Raw show

    git diff head~2..head

    git diff head..head~2

    git diff head~3:somefile.txt..head:somefile.txt  # Compare one file between commits

## commit

* __A__tomic
* __C__onsistent
* __I__ncrementa
* __D__ocumented

__Atómico__ significa que es autocontenido y coherente, cambios
relacionados deberían estar en un sólo commit, y en un commmit no
debería haber cambios mezclados.

__Consistente__ un commit debería dejar un código consistente y funcional.

__Incremental__ deberían apilarse limpiamente unos sobre otros, así
que el orden de los commits es muy importante.

__Documentado__ el mensajea asociado a un commit es
importantísimo. Debería tener un mensaje corto que sea un buen
resumen. En general es mejor documentar el "por qué" y no el "cómo".

## add

    git add -p

    git add -i
