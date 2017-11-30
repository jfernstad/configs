# Bash
Nice to have in `.bashrc` or `.bash_profile` or `.profile`.

```bash
alias ls='ls -al'
alias pods='kubectl get pods'
alias svc='kubectl get svc'

# Git alias
alias gs='git status '
alias ga='git add '
alias gb='git branch '
alias gc='git commit'
alias gd='git diff'
alias gk='gitk --all&'
alias gx='gitx --all'
alias got='git '
alias get='git '

# Go
alias coverage='go test -coverprofile=coverage.out && go tool cover -func=coverage.out && go tool cover -html=coverage.out'
export PATH=$PATH:$(go env GOPATH)/bin

export PS1='\[\033[0;31m\]\u\[\033[0m\]:\[\033[0;32m\]\w\[\033[0m\] \[\033[0m\]$ '
parse_git_branch() {
      git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/\[\1\]/'
}

export PS1='┌ \[\033[00;31m\][\u@\h]\[\033[00m\] \[\033[00;32m\][\w]\[\033[00m\] \[\033[01;33m\]$(parse_git_branch)\[\033[00m\]\n└ \$ '

```

This little snippet was fun to add to the prompt:

```bash
#`if [ \$? = 0 ]; then echo 👍 ; else echo 👎 ; fi`

export PS1='┌ `if [ \$? = 0 ]; then echo 👍 ; else echo 👎 ; fi` \[\033[00;31m\][\u@\h]\[\033[00m\] \[\033[00;32m\][\w]\[\033[00m\] \[\033[01;33m\]$(parse_git_branch)\[\033[00m\]\n└ \$ '

```
