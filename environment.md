# Ambiente de Desenvolvimento no Windows 10

## Chocolatey
 - [Chocolatey install](https://chocolatey.org/install)

## WSL 2
#### Etapa 1
 - Ativar todas opções do .NET Framework 3.5
 - Ativar todas opções .NET Framework 4.8 advance servicies
 - Ativar Plataforma de máquina Virtual
 - Ativar Plataforma HiperVerson do Windows
 - Ativar Subsistema do windows para Linux

 #### Etapa 2
  - Habilitar o recurso da máquina virtual
````
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
````

#### Etapa 4
 - Visualizar Versão do Linux e mudar para o WSL 2.
1.  `wsl --list --verbose` 
1. `wsl --set-version Ubuntu-20.04 2`
	nesta instalação estou utilizando o Ubuntu 20.04 LTS.

## Terminal
 #### Instalação do [Hyper](#)
##### Definir como bash padrão:
- Em configurações (CTRL + ,), encontre `shell:`
- copia o bash on Windows ou digitar `C:\\WINDOWS\\System32\\bash.exe`
 
#### Instalar Fira Code no Ubuntu WSL 2
````
sudo add-apt-repository universe && sudo apt update
sudo add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) universe"
sudo apt update && sudo apt install fonts-firacode
````

#### Instalação Zsh + OhMyZsh
````
sudo apt-get install zsh
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)
````
Adicionando com bash padrão
````
bash -c zsh
cd ~ && vim .bashrc
````
Adicione `bash -c zsh` dentro do arquivo.

Adicionando Linux como o padrão do ZSH
````
cd ~ && vim .zshrc
````
Adicione `cd ~` dentro do arquivo.
 
## Links úteis
- [Etapas de instalação manual](https://docs.microsoft.com/pt-br/windows/wsl/install-win10#manual-installation-steps)
- [Linux no Windows 10 com zsh Feliz](https://www.youtube.com/watch?v=iZaNTuNorWw&list=PLirko8T4cEmw2kCe2YEMSjxg_hydVZIR-)
- [Instalando WSL no WINDOWS 10](https://www.youtube.com/watch?v=Et04OjK8gPo) 
- [# WslRegisterDistribution failed with error 0x8007019e and 0x8000000d – WSL](https://www.thewindowsclub.com/wslregisterdistribution-failed-with-error-0x8007019e-0x8000000d)

```
