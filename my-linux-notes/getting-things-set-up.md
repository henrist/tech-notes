# Getting things set up

{% embed url="https://github.com/henrist/dotfiles" %}

## Initial setup of Ubuntu \(18.10\)

```bash
sudo apt install \
  git \
  tmux \
  htop \
  atop \
  jq \
  vim \
  curl \
  apt-transport-https \
  whois \
  git-crypt \
  s-tui

# For VirtualBox
# To be able to build guest additions
sudo apt install \
  gcc \
  make \
  perl

# Extra packages in some use cases
sudo apt install \
  nfs-common \
  sshfs

git clone https://github.com/henrist/dotfiles.git
cd dotfiles
./install.sh

git remote rm origin
git remote add origin git@github.com:henrist/dotfiles.git

# Firewall
sudo apt install \
  ufw \
  gufw

# Install Google Chrome
# https://google.com/chrome and follow instructions
# Log in to google Chrome

# Install ZeroTier VPN
# https://zerotier.com/download.shtml
sudo zerotier-cli join a84ac5c10a0b3278
# Approve on https://my.zerotier.com/

# Install Sublime Text 3
# https://www.sublimetext.com/
# See "Sublime Text 3.odt" in Dropbox

# Install Docker with Snap
sudo snap install docker
sudo snap connect docker:home :home

# Install Docekr without Snap
#sudo apt install docker.io

# Install from Snap:
# - VSCode
# - Slack

# Software from third party sources
# - Dropbox
# - Keybase
# - IntelliJ

https://sdkman.io/
```

## Zsh-setup

```bash
sudo apt install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

{% embed url="https://linuxconfig.org/learn-the-basics-of-the-zsh-shell" %}

{% embed url="https://github.com/bhilburn/powerlevel9k" %}

{% embed url="https://powerline.readthedocs.io/en/latest/installation/linux.html\#fonts-installation" %}

## Avoid sleep mode when closing laptop lid

```bash
sudo vim /etc/systemd/logind.conf
# make sure this line is present:
HandleLidSwitch=ignore
# log out and in, or restart
```

## Power setup on Thinkpad

```text
sudo apt update
sudo apt install tlp tlp-rdw tp-smapi-dkms acpi-call dkms
sudo tlp start

# See tpacpi-bat and battery thresholds
```

{% embed url="https://www.ubuntupit.com/best-things-to-do-after-installing-ubuntu/" %}

{% embed url="https://www.reddit.com/r/thinkpad/comments/89gi90/just\_got\_my\_t480\_upgraded\_it\_and\_slapped\_ubuntu/" %}

{% embed url="https://docs.google.com/document/d/1oOgurNY2wvrS6NWlcFAX82jDD3oYxvap2h5WvtQcm6M/edit" %}

## SIM setup

* Number: \*99\#
* Username: &lt;blank&gt;
* Password: &lt;blank&gt;
* APN: telenor
* Network ID: &lt;blank&gt;
* Accept roaming: Yes
* PIN: &lt;blank&gt; ??

## Specially for my T480

```text
xrandr --output eDP-1 --scale 1.5x1.5
```

