# docker-ringtools-testnet

This will set up a [LND](https://github.com/lightningnetwork/lnd) testnet node with Tor and [Ride-the-Lightning](https://github.com/Ride-The-Lightning/RTL) in just two commands.

It also synchronizes really fast because it uses [Neutrino](https://github.com/lightninglabs/neutrino), you don't have to run a full bitcoind testnet node (34 GB).  After synchronizing, the graph takes less than 750 MB.

It uses multiarch docker images, so you can run it on Raspberry Pi's, Intel and M1 Macs and perhaps even Windows if you really want but I didn't test that myself.

## Usage


1. Start all docker services `docker-compose up -d`
2. Create a testnet wallet: `docker-compose exec lnd lncli -n testnet create`
3. Now you can use RTL by going to [http://localhost:3000/](http://localhost:3000/), the password is `password1`

## How to get tBTC

There are several faucets available:
- [https://testnet-faucet.com/btc-testnet/](https://testnet-faucet.com/btc-testnet/)
- [https://coinfaucet.eu/en/btc-testnet/](https://coinfaucet.eu/en/btc-testnet/)
- [https://testnet-faucet.mempool.co/](https://testnet-faucet.mempool.co/)

Be nice and send the tBTC back after playing with it.
