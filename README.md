# Helix Ceramic

## Init

```bash
npm install --location=global @ceramicnetwork/cli
npm install --location=global @composedb/cli
```

## Start Ceramic db

```bash
npx @ceramicnetwork/cli daemon
```

## After the frist time launched daemon, you should stop it manully and edit your own `daemon.config.json`

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

## Index/Subcribe to the data model
```
composedb composite:deploy helix-composite.json --ceramic-url=http://localhost:7007 --did-private-key=$YOUR_PRIVATE_KEY
```

## Use the service from TypeScript client or start a graphQL server

