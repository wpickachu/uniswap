# uniswap

## Deploying

### Multicall

Deploy multicall contract from: https://github.com/makerdao/multicall/

```sh
web3 contract build Multicall.sol
web3 contract deploy Multicall.bin
```

Multicall deployed on mainnet at: 0x9d78c7Cd4BEa5bdBC1766d65c25bb019e8bE3D95

### WGO (wrapped GO)

Deploy contract from here: https://github.com/gnosis/canonical-weth/blob/master/contracts/WETH9.sol

```sh
web3 contract build WETH9.sol
web3 contract deploy WETH9.bin
```

Deployed on mainnet at: 0xcC237fa0A4B80bA47992d102352572Db7b96A6B5

### Factory

Deployed on mainnet at: 0x9fC5f58A815fa35a197Ef1F5038cCB8C04daE60d

### Router

Deployed on mainnet at: 0x2163405f665c249F7C0c26c3f966b195c54E477d

## Developing

Need to build sdk first:

```sh
git clone https://github.com/gochain/uniswap-sdk.git
cd uniswap-sdk
yarn build
```

Then in uniswap-interface repo, add your local dependency:

(NOTE: we could do sdk releases on GitHub instead?)

```sh
git clone https://github.com/gochain/uniswap-interface.git
cd uniswap-interface
yarn add file:/home/treeder/dev/gochain/uniswap-sdk
yarn
yarn start
```

### When changing SDK

Also, need web3-react:

```sh
# in sdk:
yarn build
# in interface:
yarn
yarn start
```
