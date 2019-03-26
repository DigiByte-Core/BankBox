<h1 align="center">
  <br>
  <br>
  DigiValut
  <br>
  <br>
</h1>

<h4 align="center">DigiAssets desktop wallet application for digital asset issuance and management.</h4>

**DigiValue** is a desktop client for the [DigiAssets protocol](https://github.com/DigiByte-Core/DigiAssets-Protocol-Specification) layered on top of the DigiByte blockchain.<br>
It utilizes [DigiAssets full-node](https://github.com/DigiByte-Core/Full-Node), which in its turn is dependant on [DigiByte-Core](https://digibyte.io), the DigiByte reference client.<br>
It downloads and maintains a copy of the blockchain **locally**, coupled with parsed DigiAssets assets layer of DigiAssets colored transactions - so it keeps the protocol true **peer-to-peer** with no dependance on external servers.

**Note:** A DigiAssets transaction, just as any other DigiByte transaction, requires a tiny amount of DGB to be transferred with it. Since the DigiValut gives full control to the user, it's up to the DigiVault client to finance DigiAssets transactions.

If you would like to deep dive to our programmatic Node.js (and browser) API for issuance and transfer of digital assets, go to [Getting started with DigiAssets SDK](https://github.com/DigiByte-Core/DigiAssets-docs/blob/master/getting_started.md).

## Get DigiVault Running on OSX
This guide assumes you already have homebrew & node installed on your Mac. If not read here: https://brew.sh/ for brew instalation.

Then:
```sh
$ brew install node
```

### Prerequisites

* [DigiByte-Core](https://www.digibyte.io/digibyte-wallet-downloads)
* [Redis](https://redis.io/)<br>* 
* [Node v8.11.3](https://nodejs.org/en/)<br>

### Install DigiByte Core Wallet
Download Latest DigiByte Core Wallet
https://github.com/digibyte/digibyte/releases

Navigate to DigiByte Data directory ~/Libary/Application Support/DigiByte

You might need to show hidden files on your mac in terminal with: 
```sh
$ defaults write com.apple.finder AppleShowAllFiles YES
```
Relaunch terminal/finder

Create digibyte.conf file that looks like this and restart wallet: 
```sh
algo=scrypt
rpcport=14022
txindex=1
testnet=1
rpcuser=rpcuser
rpcpassword=rpcpass
rpcallowip=127.0.0.1
server=1
listen=1
daemon=1
deprecatedrpc=accounts
```
Will take awhile so let it run while you set the rest up.

### Install NVM with Home Brew (to control version of Node DigiVault uses)
Skip this section if you already have Node Version Manager installed.
```sh
$ brew install nvm
$ mkdir ~/.nvm/
$ code ~/.bash_profile
```
Paste This and Save
```sh
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```
Restart or source terminal.

### Install Redis Server & Start It
Open new terminal window for redis, use brew to install it and then start it.
```sh
$ brew install redis
$ redis-server /usr/local/etc/redis.conf
```
### Get the DigiVault code

```sh
$ git clone https://github.com/DigiByte-Core/DigiVault.git
$ cd DigiVault
```

### Install Deps & Run DigiVault

```sh
$ nvm install 8.11.3
$ node -v
$ npm install
$ npm start
```

### Watch the code

Restart the app automatically every time code changes. Useful during development.

```sh
$ npm run watch
```

### Package the app

Builds app binaries. Currently, only Windows is available.

```sh
$ npm run package -- [options]
```

For `[options]` the following optional arguments are available:

- `--sign` - Sign the application
- `--package=[type]` - Package single output type.
  - `exe` - Windows installer
  - `portable` - Windows portable app
  - `all` - All available package options

## Support

You can find support at our [Telegram](https://t.me/DigiByteDevelopers), or e-mail us to dev@digibyte.io.

## License

[AGPL-3.0](https://www.gnu.org/licenses/agpl-3.0.en.html)


