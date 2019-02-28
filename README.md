# Blockchain BigchainDB
Tutorial for BigchainDB (v2.0.0b8) blockchain network

## Requirements
- VirtualBox
- Python
- GIT

## Instructions
### Test Server
```sh
$ git clone https://github.com/bigchaindb/bigchaindb.git
$ cd bigchaindb
$ make run
```

### Setup BigchainDB
#### Install BigchainDB Server
```sh
$ sudo apt install -y python3-pip libssl-dev
```
Fix Error: Unable to locate package python3-pip:
```sh
$ sudo nano /etc/apt/sources.list
```
Add:
- deb http://archive.ubuntu.com/ubuntu bionic main universe
- deb http://archive.ubuntu.com/ubuntu bionic-security main universe 
- deb http://archive.ubuntu.com/ubuntu bionic-updates main universe
```sh
$ sudo apt update && sudo apt upgrade
$ sudo apt install -y python3-pip libssl-dev
$ sudo pip3 install bigchaindb==2.0.0b8
```

#### Configure BigchainDB Server
```sh
$ bigchaindb configure
```

#### Configure BigchainDB Server
```sh
$ bigchaindb configure
```
Note: Accept the default value for all other BigchainDB config settings.

#### Install (and Start) MongoDB
```sh
$ sudo apt install mongodb
```

#### Install Tendermint
```sh
$ sudo apt install -y unzip
$ wget https://github.com/tendermint/tendermint/releases/download/v0.22.8/tendermint_0.22.8_linux_amd64.zip
$ unzip tendermint_0.22.8_linux_amd64.zip
$ rm tendermint_0.22.8_linux_amd64.zip
$ sudo mv tendermint /usr/local/bin
```

#### Start Configuring Tendermint
```sh
$ tendermint init
```

#### Start BigchainDB Server
```sh
$ $ bigchaindb start
```
Check BigchainDB API: http://localhost:9984/api/v1/


## References
https://www.bigchaindb.com/

https://docs.bigchaindb.com/en/latest/

https://github.com/bigchaindb/bigchaindb
