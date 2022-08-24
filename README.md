# Transfer SOL

Simple example of transferring lamports (SOL).

### Creating the example keypairs:

```shell
solana-keygen new --no-bip39-passphrase -o transfer-sol/accounts/ringo.json
```

### Viewing their public keys:

```shell
solana-keygen pubkey transfer-sol/accounts/george.json
```

```shell
Ringo:      9aomGP6bJzqfTrjMJ2YwmvjJRkP3N1MRubNAeqBqiYtX
George:     4FRvruSHJ1JiEJ2JwKbJuBHZBRhCTUx1dDgtCkm9Tkz3
Paul:       GcwKi7RtFgbHc6NZeLk3vTFotF1ifsfBzg1v4p8msTzm
John:       9PRg6RBRuKNz5jXTo9NK86sArFZ4zoX5bw15PmSDZUdk
```

### Airdropping:

```shell
solana airdrop --keypair transfer-sol/accounts/john.json 2
```

### Viewing their balances:

```shell
solana account <pubkey> 
```

## Run the example:

In one terminal:
```shell
npm run reset-and-build
npm run simulation
```

In another terminal:
```shell
solana logs | grep "<program id> invoke" -A 7
```