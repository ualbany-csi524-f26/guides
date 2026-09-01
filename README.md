# Guides
## Set up SEED virtual machine on a Windows or (older) Mac with Intel chipset
1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads) for your machine.
2. Download [SEED Ubuntu 20.04 VM image zip file](https://drive.google.com/file/d/15T375oNM95uS98PEpGkbPqo1kFFwarEB/view?usp=sharing) (MD5 checksum: f3d2227c92219265679400064a0a1287). 
  - Note: The download size is about 4GB, and you should account for another 20GB for the unpacked VM.
3. Unzip the image and follow the [SEED VM instructions](./seedvm-manual.md) to load the image into VirtualBox.

## Set up SEED virtual machine on Apple Silicon Mac
### Install using UTM
1. Install [UTM](https://mac.getutm.app/).
2. The original SEED Labs Ubuntu installation for Mac uses VMWare Fusion as the virtualization software. Please follow the same [instructions for VMWare](./seedvm-arm64-ubuntu-installation.md), however, use UTM instead. Steps:
    1. Select "Create A NEw Virtual Machine".
    2. Select "Virtualize".
    3. Select "Linux".
    4. Make sure "Use Apple Virtualization" is checked (selected).
    5. Select your iso file and continue installation as in the original instructions. 
6. Install software inside the VM to get the required environment of SEED labs: [SEED Labs software installation](./seedvm-arm64-lab-setup.md).
### Install using VMWare Fusion
Please note that students have faced issues installing Ubuntu 22.04 on VMWare Fusion. We recommend that use UTM instead as your virtualization software.
1. Install VMware Fusion (which is free for personal use). A detailed instruction is provided in [seedvm-arm64-fusion-installation.md](./seedvm-arm64-fusion-installation.md).
2. Build an Ubuntu VM on VMWare Fusion. Since the desktop versions of all Ubuntu VM are removed, we can no longer use the pre-built desktop versions. We install the server version instead, but don't worry about the GUI, as we will install ubuntu-desktop in the VM later. A detailed instruction is provided in [seedvm-arm64-ubuntu-installation.md](./seedvm-arm64-ubuntu-installation.md).
3. Install software inside the VM to get the required environment of SEED labs: [SEED Labs software installation](./seedvm-arm64-lab-setup.md).

## SEED manual for docker containers
Refer to [SEED Labs manual for containers](https://github.com/seed-labs/seed-labs/blob/master/manuals/docker/SEEDManual-Container.md).

## GitHub access token
GitHub has discontinued accepting passwords as an authentication mechanism when you work with it from shell. Instead of password, you need to [create and use an access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) (**classic access token**, not fine-grained token).

Make sure you store this token in a secure place (e.g., a password manager) to reuse it. If you loose the token, you can regenerate a new one.

## Enable SSH access to GitHub
Accessing GitHub via SSH is generally considered more secure than using username and secret-token. As an additional benefit, you can use an SSH agent to automate the remote authentication process so that you would not need to provide your username/token every time that you interact with GitHub (git clone/push/pull).

Follow the [GitHub SSH access instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

For further instructions on setting up SSH, see [ArchWiki's article on SSH keys](https://wiki.archlinux.org/title/SSH_keys).
