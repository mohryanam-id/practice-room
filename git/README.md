# Git

## Git Config
### Environment Variables
add environment variable in your .zshrc/.bashrc
```bash
export GIT_USER_NAME="<name>"
export GIT_USER_EMAIL="<email>"
```

### Commands
Configuring user information used across all local repositories.
```bash
git config --global user.name "$GIT_USER_NAME"
git config --global user.email "$GIT_USER_EMAIL"
```

## SSH Config
### Generate SSH Key
```bash
ssh-keygen -t rsa -C $GIT_EMAIL
```
### Copy Public Key
Copy content from
```bash
cat /home/<your_user>/.ssh/id_rsa.pub
```

### Paste Public Key (Github)
click Settings > click SSH and GPG keys > click New SSH Key > fill Title box > paste on Key box
 
### Clone Repository Using SSH (Github) 
```bash
git clone git@github.com:<username>/<repository>.git
```
