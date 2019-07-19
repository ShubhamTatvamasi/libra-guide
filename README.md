# libra-guide

### Setup Libra

1. Clone Libra:
```bash
git clone https://github.com/libra/libra.git && cd libra
```

2. Install Dependencies:
```bash
./scripts/dev_setup.sh
```

3. Run the CLI:
```bash
./scripts/cli/start_cli_testnet.sh
```
---

### Setup Accounts

1. Create an account
```
account create
```

2. See the list of accounts
```
account list
```
---

### Add coins to account

1. Mint 100 coins on account 0
```
account mint 0 100
```

2. Check balance of account 0
```
query balance 0
```
---

### Submit a Transaction

1.Query the Accounts’ Sequence Numbers
```
query sequence 0
```
> this is same as transaction nonce in ethereum

2. Transfer 10 coins from account 0 to 1
```
transfer 0 1 10
```

3. Get transaction info
```
query txn_acc_seq 0 0 false
```
> The first parameter is the local index of the sender account, and the second parameter is the sequence number of the account.
