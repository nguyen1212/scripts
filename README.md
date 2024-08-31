## Oh-My-Zsh

### Plugins

CLI:Auto-suggestion
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Env

### Direnv

ENV: sub-direnv
```
source_up

export VAR=value
```

## Docker

### Colima

CLI
```
brew install colima
brew services start colima // start colima when restart
colima start
```

ENV
```
DOCKER_HOST=unix:///$HOME/.colima/default/docker.sock // set docker host to docker daemon socket

