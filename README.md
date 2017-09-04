# GGCRYPTO

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

Install build dependencies

`sudo apt-get install build-essential git cmake libboost1.55-all-dev`

Clone the repository:

`git clone https://github.com/ggcrypto/ggcrypto`

Build

`cd ggcrypto; make`

Link to path

```
mkdir $HOME/bin
cd $HOME/bin
ln -s $HOME/ggcrypto/build/release/src/simplewallet ggcryptowallet
ln -s $HOME/ggcrypto/build/release/src/ggcryptod
ln -s $HOME/ggcrypto/build/release/src/walletd
```

Run

`ggcryptod` to start a node
`ggcryptowallet` to start you wallet

Mining

Inside `ggcryptowallet` shell type:

`start_mining`

Profit!



## CryptoNote

This is the reference code for [CryptoNote](https://cryptonote.org) cryptocurrency protocol.

* Launch your own CryptoNote currency: [CryptoNote Starter](https://cryptonotestarter.org/)
* CryptoNote reference implementation: [CryptoNoteCoin](https://cryptonote-coin.org)
* Discussion board and support: [CryptoNote Forum](https://forum.cryptonote.org)
