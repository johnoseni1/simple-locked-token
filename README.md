

## Usage

Clone or donwload this repositorie.

Go to path and run on terminal:

```sh
npm install
```
After running, all dependecies will be downloaded.

Maybe you need install truffle as global dependency to run next steps.

### Compile contracts

```sh
truffle compile
```

After running, contract information &mdash; including ABI &mdash; will be available at the `build/contracts/` directory.

### Run tests on Truffle

You can run tests which can be found in the test directory `/test` runing on terminal:

```sh
truffle test
```

Or run tests within a specific file:

```sh
truffle test <file_path>
```

### Run migration and deploy contracts

Create .env file on root with:

```
PRIVATE_KEY = // Wallet private key
INFURA_PROJECT_ID = // Your Infura Project Id
TOKEN_NAME = "Token Name"
TOKEN_SYMBOL = "ERC"
TOKEN_DECIMALS = 18
TOKEN_TOTALSUPLY = 0
```

It is important that the chosen wallet has native tokens for the payment of gas.

Run migrate command:

```sh
truffle migrate --network <network_name> // mainnet, rinkeby, polygon, mumbai...
```

After migration, contract address and transaction ID will be shown on screen.
