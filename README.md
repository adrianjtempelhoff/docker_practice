# docker_practice
Examples and practice with docker

Official site: 
https://www.docker.com/

Documentation: 
https://docs.docker.com/

Installation on Linux: _(foolowing guide from https://techviewleo.com/how-to-install-and-use-docker-in-linux-mint/)_
Update your system
First ensure that your system packages are updated
**sudo apt-get update**

Install Docker dependencies and add Docker official key
APT does not use HTTPS and it is crucial to install the packages and dependencies that will enable it to use a repository through https
**sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common**

Next add Docker official key which is important in enabling Docker repo.
**curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -**

Adding Docker repository
Next thing is to add Docker repository to Linux Mint. The variable ‘$ (. /etc/os-release; echo “$ubuntu-codename”)’ ensures that you are using the right distribution of your Linux Mint
**sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(. /etc/os-release; echo "$UBUNTU_CODENAME") stable"**

Update your system again
**sudo apt-get update**

Install Docker CE on Linux Mint 20
Run the below command to install the latest version of Docker CE
**sudo apt-get -y install docker-ce**

Once installed a docker group will be created. Add your user to the group who will be running docker commands.
**sudo usermod -aG docker $USER**
**newgrp docker**

Verify Docker Installation
Show docker version
**docker --version**

The output should show docker version and build
Some Docker commands

Docker is used with syntax as shown below:
**docker [options] [command] [arguments]**

To check options to be used with docker, run:
**docker**
or
**docker help**


