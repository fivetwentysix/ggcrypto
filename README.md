# GGCRYPTO

Disclaimer: This is a experimental project. We may discontinue this and fork at anytime.
Treat involvement as educational purposes only. There is no guarentee or even likelyness of these tokens
ever being worth anything.

GGCRYPTO is based on CryptoNote. This is the repository to explore the codebase of the blockchain.

## Setting up a node and wallet on Ubuntu 14.04

You can get one Virtual Machine in the cloud with many well known providers:

* Rackspace
* AWS EC2
* Google Compute Engine
* Alibaba Cloud
* [Digital Ocean](https://m.do.co/c/a03123d75450)
* And more rougly $30 usd a month

Tested with 4GB ram and above.

Shell into your server with either SSH keys (preferred) or username and password. Try [Chrome Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo?hl=en) which is a SSH addon for Chrome.

## Setting up

Install the build dependencies running this command:

```
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install build-essential git cmake libboost1.55-all-dev
```

Clone the repository:

`git clone https://github.com/ggcrypto/ggcrypto`

## Build

`cd ggcrypto; make`

Link to path

```
mkdir $HOME/bin
cd $HOME/bin
ln -s $HOME/ggcrypto/build/release/src/simplewallet ggcryptowallet
ln -s $HOME/ggcrypto/build/release/src/ggcryptod
ln -s $HOME/ggcrypto/build/release/src/walletd
```

## Run

* `ggcryptod` to start a node
* `ggcryptowallet` to start you wallet

## Mining

Inside `ggcryptowallet` shell type:

`start_mining`

Profit!

## Terminal Split Screen & Keep Alive

I suggest using TMUX which can be installed using `sudo apt-get install -y tmux`

To start TMUX: `tmux new`

You can press:

* `CTRL + B`, `ARROW_KEY`
* `CTRL + B`, `%`
* `CTRL + B`, `"`

to split and navigate windows

Closing the shell running a TMUX instance does not close TMUX so this is a great way to run both the node and the wallet indefinately.
