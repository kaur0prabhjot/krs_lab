**Docker**

**\#Pre-requisite:**

sudo apt install gnome-terminal

**\#Set up Docker's apt repository:**

\# Add Docker's official GPG key:

sudo apt-get update

sudo apt-get install ca-certificates curl

sudo install \-m 0755 \-d /etc/apt/keyrings

sudo curl \-fsSL https://download.docker.com/linux/ubuntu/gpg \-o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

\# Add the repository to Apt sources:

echo \\

  "deb \[arch=$(dpkg \--print-architecture) signed-by=/etc/apt/keyrings/docker.asc\] https://download.docker.com/linux/ubuntu \\

  $(. /etc/os-release && echo "${UBUNTU\_CODENAME:-$VERSION\_CODENAME}") stable" | \\ sudo tee /etc/apt/sources.list.d/docker.list \> /dev/null

sudo apt-get update

**\#Install the Docker packages:**

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

**\#Verify that the installation:**

sudo docker run hello-world

**\#Download the latest deb package from** https://desktop.docker.com/linux/main/amd64/docker-desktop-amd64.deb?utm\_source=docker\&utm\_medium=webreferral\&utm\_campaign=docs-driven-download-linux-amd64

**\#Install the package using apt:**

sudo apt-get update

sudo apt-get install ./docker-desktop-amd64.deb

\# You can ignore this error message:

N: Download is performed unsandboxed as root, as file '/home/user/Downloads/docker-desktop.deb' couldn't be accessed by user '\_apt'. \- pkgAcquire::Run (13: Permission denied)

**\#Usage:**

\#To run docker from terminal:

systemctl \--user start docker-desktop

\#Alternatively, docker desktop application should be present in your Gnome/KDE Desktop.