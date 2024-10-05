# deploy-golang-project / Hello Ubuntu Server

## Hello World project on Ubuntu Server
- Standard Go Project Layout: https://github.com/golang-standards/project-layout/
- Backend: goFiber
- Frontend: ReactJS + Bootstrap@5.3.3
- Install Nginx Server
- Create certbot: SSL Certificate: asakew.ru
- DockerFile + DockerCompose: if the server restarts the container should also automatically start.

## Features
- Deploy Golang project to Ubuntu server
- VIM Editor
- Install-zsh + Add Custom Theme + Auto-Suggestions + Syntax-highlighting
- Git
- Install Golang@latest version
- Docker@latest version
___________________

## Connecting Ubuntu Server
Connecting via SSH / your IP address and your Password
```bash
ssh root@192.168.1.5
```

## Update Ubuntu Server and Install-zsh
```bash
sudo apt update && apt list --upgradable && sudo apt install zsh -y && zsh --version && sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)" 
```

## Add a Custom Theme and Auto-Suggestions/Syntax-highlighting
### Edit file ~/.zshrc
```bash
vim ~/.zshrc
```

## Add Custom Theme and Auto-Suggestions/Syntax-highlighting
```bash
.zshrc file add: ZSH_THEME="jonathan"
.zshrc file add: plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

## Clone Auto-Suggestions/Syntax-highlighting and Restart Ubuntu server
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions && git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting && sudo reboot
```
___________________

## VIM Editor commands:
- normal mode: a
- i - insert/edit mode
- v - visual mode
- esc - exit visual mode
- shift + : and wq - save and exit
- full exit: shift + z + z

- dd - delete line
- y - copy line
- p - paste line

- u - undo
- r - redo
- w - save
- shift + : and wq - save and exit
- :q - exit

- how save file: :w
- gg - up line
- G - down line

https://www.youtube.com/watch?v=8KbM86FfTCQ/
https://www.youtube.com/watch?v=6H0GDM8ExB8/

## Delete Files on Linux Terminal
* rm file_1.txt / rm file_2.txt file_3.txt
* rm ./path/to/the/file/file_1.txt

- Docs: https://www.howtogeek.com/409115/how-to-delete-files-and-directories-in-the-linux-terminal/
___________________

## Repeat Connecting Ubuntu Server
Connecting via SSH / your IP address and your Password
```bash
ssh root@192.168.1.5
```

## Install Git
```bash
sudo apt update && apt list --upgradable && sudo apt install git
```

## Setup SSH in GitHub by example:
Docs: https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/GitHub-SSH-Key-Setup-Config-Ubuntu-Linux/
___________________

## Install Golang
```bash
sudo apt update && apt list --upgradable && sudo snap install go  --classic && go version
```

## Ubuntu server clone Golang project
```bash
git clone https://github.com/asakew/deploy-golang-project.git
```
___________________

## Install Docker@latest version
Docs: https://docs.docker.com/engine/install/ubuntu/

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```


```bash
docker build -t your-image-name . --progress=plain ## build your docker image
```


##  Install Nginx on Ubuntu Server
```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx

```