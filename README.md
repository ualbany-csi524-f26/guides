# Guides
## Set up SEED virtual machine on a Windows or (older) Mac with Intel chipset
1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads) for your machine.
2. Download [SEED Ubuntu 20.04 VM image zip file](https://drive.google.com/file/d/15T375oNM95uS98PEpGkbPqo1kFFwarEB/view?usp=sharing) (MD5 checksum: f3d2227c92219265679400064a0a1287). 
  - Note: The download size is about 4GB, and you should account for another 20GB for the unpacked VM.
3. Unzip the image and follow the [SEED VM instructions](./seedvm-manual.md) to load the image into VirtualBox.

## Set up SEED virtual machine on Apple Silicon Mac
1. Install VMware Fusion (which is free for personal use). A detailed instruction is provided in [seedvm-arm64-fusion-installation.md](./seedvm-arm64-fusion-installation.md).
2. Build an Ubuntu VM on VMWare Fusion. Since the desktop versions of all Ubuntu VM are removed, we can no longer use the pre-built desktop versions. We install the server version instead, but don't worry about the GUI, as we will install ubuntu-desktop in the VM later. A detailed instruction is provided in [seedvm-arm64-ubuntu-installation.md](./seedvm-arm64-ubuntu-installation.md).
3. Install software inside the VM to get the required environment of SEED labs. A detailed instruction is provided in [seedvm-arm64-lab-setup.md](./seedvm-arm64-lab-setup.md).

## SEED manual for docker containers
Refer to [SEED Labs manual for containers](https://github.com/seed-labs/seed-labs/blob/master/manuals/docker/SEEDManual-Container.md).

## GitHub access token
GitHub has discontinued accepting passwords as an authentication mechanism when you work with it from shell. Instead of password, you need to [create and use an access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) (**classic access token**, not fine-grained token).

Make sure you store this token in a secure place (e.g., a password manager) to reuse it. If you loose the token, you can regenerate a new one.

## Enable SSH access to GitHub
Accessing GitHub via SSH is generally considered more secure than using username and secret-token. As an additional benefit, you can use an SSH agent to automate the remote authentication process so that you would not need to provide your username/token every time that you interact with GitHub (git clone/push/pull).

Follow the [GitHub SSH access instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

For further instructions on setting up SSH, see [ArchWiki's article on SSH keys](https://wiki.archlinux.org/title/SSH_keys).
