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
colima start --mount-type 9p
```

ENV
```
# zshrc
export DOCKER_HOST=unix:///$HOME/.colima/default/docker.sock // set docker host to docker daemon socket

# /Users/<username>/.colima/_lima/_config/override.yaml
mountType: 9p
mounts:
  - location: "/Users/<username>"
    writable: true
    9p:
      securityModel: mapped-xattr
      cache: mmap
  - location: "~"
    writable: true
    9p:
      securityModel: mapped-xattr
      cache: mmap
  - location: /tmp/colima
    writable: true
    9p:
      securityModel: mapped-xattr
      cache: mmap
```



## Node

### NVM

CLI
```
brew install nvm
nvm install v16.20.2 // install specific node version
```

ENV
```
export NVM_DIR="$HOME/.nvm"
  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" 
```
