# Helix Ceramic

## Init

```bash
npm install --location=global @ceramicnetwork/cli
npm install # in the project dir
```

## Start Ceramic db

```bash
npx @ceramicnetwork/cli daemon
```

## Using your account

```bash
# Generate private key
composedb did:generate-private-key
export CERAMIC_PRIVATE_KEY=<your private key>
# Generate DID
composedb did:from-private-key your-private-key
cd ~/.ceramic
vim daemon.config.json
# put your did in "admin-dids"
# Restart ceramic
ceramic daemon --network=inmemory/testnet-clay/mainnet
```
