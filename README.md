<h1 align="center">
  <br>
  <br>
  DigiValut
  <br>
  <br>
</h1>

<h4 align="center">DigiAssets desktop wallet application for digital asset issuance and management.</h4>

**DigiValue** is a desktop client of the [DigiAssets protocol](https://github.com/DigiByte-Core/DigiAssets-Protocol-Specification) on top of the DigiByte blockchain.<br>
It utilizes [DigiAssets full-node](https://github.com/DigiByte-Core/Full-Node), which in its turn is dependant on [DigiByte-Core](https://digibyte.io), the DigiByte reference client.<br>
It downloads and maintains a copy of the blockchain **locally**, coupled with parsed DigiAssets assets layer of DigiAssets colored transactions - so it keeps the protocol true **peer-to-peer** with no dependance on external servers.

**Note:** A DigiAssets transaction, just as any other DigiByte transaction, require a tiny amount of DGB to be transferred with it.
Since the DigiValut gives full control to the user, it's up to the DigiVault client to finance DigiAssets transactions.

If you would like to deep dive to our programmatic Node.js (and browser) API for issuance and transfer of digital assets, go to [Getting started with DigiAssets SDK](https://github.com/DigiByte-Core/DigiAssets-docs/blob/master/getting_started.md).

## Prerequisites

* [DigiByte-Core](https://www.digibyte.io/digibyte-wallet-downloads)
* [Redis](https://redis.io/)<br>

Windows installer will download these dependencies for you, but for other OS they should be installed separately.

## Install

<b>Download the latest version of DigiVault from the
[GitHub releases](https://github.com/DigiByte-Core/DigiVault/releases) page </b> (currently not available)

### OR

You can run from source.<br>
First you need to download the prerequisites mentioned above, and then use the instructions in the ["How to Contribute"](#how-to-contribute) section.

## Screenshots

<p align="center">
  <img src="http://coloredcoins.org/img/bankbox-screenshot-dashboard.JPG" alt="screenshot" height="750" align="center">
  <div style="margin-bottom: 16px;"/>
  <img src="http://coloredcoins.org/img/bankbox-screenshot-transaction.JPG" alt="screenshot" height="750" align="center">
</p>

## Configuration

DigiVault comes with default properties - such as the DigiByte network (mainnet or testnet), default transaction fee and the configuration for the DigiAssets full-node server, DigiByte-Core daemon and Redis. <br>
DigiAssets `properties.conf` can be found and edited in: <br>
`%APPDATA%\DigiAssets` (windows) <br>
DigiAssets full-node `properties.conf`: <br>
`%APPDATA%\digiassets-full-node` (windows)

## How to Contribute

### Get the code

```sh
$ git clone https://github.com/DigiByte-Core/DigiVault.git
$ cd DigiVault
$ npm install
```

### Run the app

```sh
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


