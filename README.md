# Wallet Ðapp

A basic DApp wallet for the Ethereum Network. 

	- ** NOTE ** This is not an official release.
	More updates to come in the near future! For now this can be run on a local 
	machine, or used for learning purposes. LICENSE specifies use of the code contained in this repository.

(Disregard this build status bar. This is not to be considered a finished project. Leave this here for later because it will be good documentation)

[![//Build Status](https://travis-ci.org/ethereum/meteor-dapp-wallet.svg?branch=master)](https://travis-ci.org/ethereum/meteor-dapp-wallet)


## Installations
	** Note: include build directions for all machines **

	- Go-Ethereum (and all things needed for that)
	- Node, npm, homebrew (essentials all programmers should have)
	- Meteor (and all of the associated packages)
	

## Development

Start an `geth` node and and the app using meteor and open http://localhost:3000 in your browser:

    $ geth --rpccorsdomain "http://localhost:3000" --rpc --port 0

Starting the wallet dapp using [Meteor](https://meteor.com/install)

    $ cd meteor-dapp-wallet/app
    $ meteor

Go to http://localhost:3000


## Deployment

To create a build version of your app run:
    
    // install meteor-build-client
    $ npm install -g meteor-build-client

    // bundle dapp
    $ cd meteor-dapp-wallet/app
    $ meteor-build-client ../build --path ""

This will generate the files in the `../build` folder. Double click the index.html to start the app.
To make routing work properly you need to build it using:

    $ meteor-build-client ../build

And start a local server which points with its document root into the `../build` folder,
so that you can open the app using `http://localhost:80/`


***
(Not our stats... Utilize this later for documentation)
## Gas usage statistics

- Deploy original wallet: 1 230 162
- Deploy wallet stub: 184 280
- Simple Wallet transaction: 64 280
- Multisig Wallet transaction below daily limit: 79 280
- Multisig Wallet transaction above daily limit: 171 096
- 1 Multisig confirmation: 48 363
