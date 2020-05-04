# Install MicroKube For version peatio 2.3.11 in Ubuntu 18.04 Documented by poseidon ~ telegram id: @pos3idon (Demo https://coincooper.com ) soon update document for ubuntu 20.04.

## Step 1: Install Docker

To install Docker you will need to do those steps with `sudo` or login as root user with `sudo -i`

Create a Unix user for holding your application
```
sudo adduser app
sudo usermod -a -G sudo app

```

### Installing from apt-get

First, update your existing list of packages:

```
apt update
```

Next, install a few prerequisite packages which let apt use packages over HTTPS:

```
apt install apt-transport-https ca-certificates curl software-properties-common -y
```

Then add the GPG key for the official Docker repository to your system:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
```

Add the Docker repository to APT sources:

```
add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```

Next, update the package database with the Docker packages from the newly added repo:

```
apt update
```

Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:

Finally, install Docker:

```
apt install docker-ce -y
```

Docker should now be installed, the daemon started, and the process enabled to start on boot. Check that it's running:

```
systemctl status docker
```

Add your app user into the docker group

```
usermod -aG docker app
```

## Step 2: Install Docker Compose

Run this command to download the latest version of Docker Compose:

```
curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose
```

## Step 3: Clone MicroKube

Login to your app user:
```
su - app

```
Install Ruby
```
sudo apt-get install git curl zlib1g-dev build-essential \
           libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 \
           libxml2-dev libxslt1-dev libcurl4-openssl-dev libffi-dev -y
```
Installing rvm
```
gpg --keyserver hkp://keys.gnupg.net \
             --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 \
                         7D2BAF1CF37B13E2069D6956105BD0E739499BDB

 \curl -sSL https://get.rvm.io | bash -s stable --ruby=2.6.0 --gems=rails
```
Source RVM


```
source /home/app/.rvm/scripts/rvm
rvm use 2.6.0
```

Clone microkube repository
```
cd $HOME
git clone https://github.com/poseidon-j/microkube-for-2.3.11.git
cd microkube-for-2.3.11
```

## Step 4: Clone your frontend

Edit config file `config/app.yml`

DO `rake service:all` couples of times


# username and password:   
  
 - email: admin@barong.io
 
   password: `YOU WILL GET IT IN TERMINAL WHILE BARONG RUN`
  
   role: admin
    
 - email: john@barong.io
  
   password: Am8icnzEI3d!
  
   role: member
   
   
