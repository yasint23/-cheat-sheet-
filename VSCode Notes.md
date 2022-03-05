1- Change the name as “slave” of ec2 on Vs Code by
```
sudo hostnamectl set-hostname slave

2- Make colour the ec2 on vscode terminal
```
export PS1="\[\e[36m\]\u\[\e[m\]@\h-\w:\[\e[31m\]\\$\[\e[m\] "

3- Make colour and shows the branch on the git local-remote repo
```
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\[\e[36m\]\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "

4- Get the public ip from terminal, you can play the command...
```
curl http://169.254.169.254/latest/meta-data/public-ipv4