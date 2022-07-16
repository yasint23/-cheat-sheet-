1- Make colour and shows the branch on the git local-remote repo (Hepsini tek seferde kopyalayip run edeceksin)
```
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\[\e[36m\]\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "

Bu komutlari, ec2 icerisindeki ".bashrc" file icine kopyalayip, ec2 stop run edince terminale "bash" yazarak activite edebilirsin.
 

2- Get the public ip from terminal, you can play the command...
```
curl http://169.254.169.254/latest/meta-data/public-ipv4

3- Host *
    TCPKeepAlive yes
    ServerAliveInterval 120

Host my-ubuntu 
    HostName 34.236.171.28
    IdentityFile C:\Users\pakya\.ssh\yasin.pem
    User ubuntu

Host my-linux 
    HostName 44.202.14.220
    IdentityFile C:\Users\pakya\.ssh\yasin.pem
    User ec2-user