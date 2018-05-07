# bash-commands

############################
# INSTRUCTIONS
# 1. Install git bash
# 2. cd ~
# 3. vi .bashrc
# 4. copy everything below the instructions
# 5. paste into vim
# 6. WIN!
############################

alias cdu="cd .. && ls"

############################ 
# Git shorthand 
############################ 
alias g="git" 
alias ga="git add" 
alias gap="git add -p" 
alias gc="git commit" 
alias go="git checkout" 
alias gp="git push"
alias gs="git status" 
alias grb="git rebase -i" 
alias grbc="git rebase --continue" 
alias grba="git rebase --abort" 
alias grbm="git rebase master" 
alias gcp="git cherry-pick" 
alias gd="git diff" 
alias gclean="git clean -fd" 
alias gb="git branch" 
alias gmf="git merge --ff-only"

############################ 
# Git compound commands 
############################ 
alias gup="git pull --rebase && git remote update origin --prune" 
alias gbail="git reset --hard HEAD@{upstream} && git clean -fd" 
alias glog="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %Cblue<%an>%Creset' --abbrev-commit --date=relative" 

############################ 
# Shortcut to Atom 
############################ 
alias a="atom ."

############################ 
# Clean and reinstall node and bower dependencies 
############################ 
alias depclean="rm -rf node_modules bower_components && npm i && bower i" 
alias yarndepclean="rm -rf node_modules bower_components && yarn install && bower i"

############################ 
# Better ls output 
############################ 
alias ls="ls --color=auto -alhX"

############################ 
# Create new branch and push to github 
############################ 
gnew() {   
	local branchName=$1   
	git checkout -b $branchName   
	git push --set-upstream origin $branchName 
}
