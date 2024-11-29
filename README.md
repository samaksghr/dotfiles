# .dotfiles
## Requirements
Make sure to install 1Password. Check https://support.1password.com/install-linux/.\
\
Then add the following config in ``~/.config/1Password/ssh/agent.toml ``.
```bash
[[ssh-keys]]
item = "Name"
vault = "Personal"
```
Test if ssh-agent can list your keys :
```bash
SSH_AUTH_SOCK=~/.1password/agent.sock ssh-add -l
```
```bash
256 SHA256: ... Name (ED25519)
...
```
## Installing
```bash
git clone --bare git@github.com:samaksghr/dotfiles.git $HOME/.dotfiles
git --git-dir=$HOME/.dotfiles --work-tree=$HOME checkout main
```