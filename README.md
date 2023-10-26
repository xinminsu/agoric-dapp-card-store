# Baseball Card Store Dapp

TL;DR:

The Baseball Card Store Dapp sells baseball cards as NFT tokens in
exchange for money.

Install the
[prerequisites](https://agoric.com/documentation/getting-started/before-using-agoric.html).

### Execute every command below in a seperate terminal

Install the sdk
```sh
git clone --branch multi-users https://github.com/xinminsu/agoric-sdk
cd agoric-sdk
yarn && yarn build
```

Install the dapp
```sh
git clone https://github.com/xinminsu/agoric-dapp-card-store.git
cd agoric-dapp-card-store
agoric install
```

Start your local-chain
```sh
cd agoric-sdk/packages/cosmic-swingset
make scenario2-setup && make scenario2-run-chain
```

Start `ag-solo`
```sh
cd agoric-sdk/packages/cosmic-swingset
make scenario2-run-client
```

Start `ag-solo-1`
```sh
cd agoric-sdk/packages/cosmic-swingset
make scenario2-run-client-1

Open your wallet UI
```sh
cd agoric-sdk/packages/cosmic-swingset/t1/8000
agoric open --repl --hostport=localhost:8000
```

Open your wallet UI 1
```sh
cd agoric-sdk/packages/cosmic-swingset/t1/8001
agoric open --repl --hostport=localhost:8001
```

Deploy the contract
```sh
cd agoric-dapp-card-store
agoric deploy contract/deploy.js api/deploy.js
```

Start UI, 
```sh
# Navigate to the `ui` directory and start a local server
cd agoric-dapp-card-store/ui && yarn start
```

## Using the Dapp

1. A window for your wallet should open.
4. Under "Dapps" in the wallet, enable the CardStore Dapp.
5. Now you should be able to click on a card to make an offer to buy
   it.
6. Approve the offer in your wallet
7. View the card in your wallet.

![Card Store](./readme-assets/card-store.png)

To learn more about how to build Agoric Dapps, please see the [Dapp Guide](https://agoric.com/documentation/dapps/).

See the [Dapp Deployment Guide](https://github.com/Agoric/agoric-sdk/wiki/Dapp-Deployment-Guide) for how to deploy this Dapp on a public website, such as https://cardstore.testnet.agoric.com/
