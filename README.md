# Instala-o-zsh-ubuntu/Debian

#!/bin/bash

# Executar comandos a seguir para atualizar os pacotes
sudo apt update -y
sudo apt upgrade -y

# Só o Python
sudo apt install python3.10-full python3.10-dev -y

# Instalar pacotes a seguir
- sudo apt install git curl build-essential dkms perl wget -y
- sudo apt install gcc make default-libmysqlclient-dev libssl-dev -y
- sudo apt install -y zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev llvm \
  libncurses5-dev libncursesw5-dev \
  xz-utils tk-dev libffi-dev liblzma-dev python3-openssl git
  
# Pyenv (gerenciador de versoes python)
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
# Seguir instruções do Pyenv

# Baixar e instalar VS Code: https://code.visualstudio.com/download

# Abaixo tudo é opcional

# Instalar e configurar ZSH
sudo apt install zsh -y
chsh -s /bin/zsh
zsh

# Instalar Oh-my-zsh! -> https://ohmyz.sh/
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Instalar Spaceship Prompt
# https://github.com/spaceship-prompt/spaceship-prompt
- git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
- ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
  

# Mudar ~/.zshrc -> ZSH_THEME="spaceship"

## colar export gerado

# Instalar Zsh Autosuggestions
# https://github.com/zsh-users/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# Instalar Zsh Syntax Highlighting
# https://github.com/zsh-users/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Mudar plugins
# plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

# Font optional (https://github.com/pdf/ubuntu-mono-powerline-ttf)
mkdir -p ~/.fonts
git clone https://github.com/pdf/ubuntu-mono-powerline-ttf.git ~/.fonts/ubuntu-mono-powerline-ttf
fc-cache -vf
- mudar a fonte em configuraçẽos para 

## https://github.com/spaceship-prompt/spaceship-prompt
- ir no site do spaceship prompt e pegar comando  

### REBOOT!!!!!!!!!!!!!!!!!!!!!



#atualizar as versoes do python 
pyenv update 


# listar todas as versões de python
pyenv install -l


# instalar uma versão especifica 
pyenv install versãoquedeseja

 # utilizar python global
 pyenv vlobal e a versãoquedesejadeixarglobal


 settings json vscode
## Configurações do VS Code

Adicione o seguinte conteúdo ao seu arquivo `settings.json` para configurar seu ambiente:

```json
{
    "workbench.startupEditor": "none",
    "editor.fontSize": 14,
    "explorer.compactFolders": false,
    "code-runner.runInTerminal": true,
    "code-runner.clearPreviousOutput": true,
    "code-runner.executorMap": {
        "javascript": "node",
        "java": "cd $dir && javac $fileName && java $fileNameWithoutExt",
        "c": "cd $dir && gcc $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
        "python": "cls ; python -u"
    },
    "code-runner.ignoreSelection": true,
    "workbench.colorTheme": "OM Theme (Default Dracula Italic)",
    "workbench.iconTheme": "material-icon-theme",
    "python.defaultInterpreterPath": "python"
}


