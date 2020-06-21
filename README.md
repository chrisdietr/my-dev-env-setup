# my-dev-env-setup
Setup of python environment.

## Ubuntu 20.04 LTS + zsh + ohmyzsh + pyenv + direnv

### Ubuntu
```
echo "Installing zsh"
sudo apt-get update; sudo apt-get install --no-install-recommends make build-essential \
libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev \
wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev \
libffi-dev liblzma-dev python-openssl git
```

### zsh
echo "Installing zsh"
sudo apt install zsh



### ohmyzsh
```
echo "Install Ohmyzsh"
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
echo "Logout and login required for activation!"
```

### pyenv
```
echo "Install pyenv https://github.com/pyenv/pyenv#installation"
curl https://pyenv.run | zsh
```

### direnv
```
sudo apt install direnv
echo '# direnv: show venv in prompt + hook to shell' >> ~/.zshrc
echo '' >> ~/.zshrc
echo 'show_virtual_env() {' >> ~/.zshrc
echo '	if [ -n "$VIRTUAL_ENV" ]; then' >> ~/.zshrc
echo '		echo "($(basename $VIRTUAL_ENV))"' >> ~/.zshrc
echo '	fi' >> ~/.zshrc
echo '}' >> ~/.zshrc
echo '' >> ~/.zshrc
echo 'PS1='$(show_virtual_env)'$PS1' >> ~/.zshrc
echo '' >> ~/.zshrc
echo 'eval "$(direnv hook bash)"' >> ~/.zshrc
```

### Reboot
```
echo "Reboot server"
sudo reboot
```