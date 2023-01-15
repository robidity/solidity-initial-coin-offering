# Solidity ICO Presale Smart Contract

![my badge](https://badgen.net/badge/license/MIT/green)

![my badge](https://badgen.net/badge/version/1.0.0/green)

![my badge](https://badgen.net/badge/icon/8.5.5/green?icon=npm&label)

![my badge](https://badgen.net/badge/nodejs/16.15.0/green)

![my badge](https://badgen.net/badge/truffle/5.5.9/green)

![my badge](https://badgen.net/badge/solidity-compiler/0.8.13/green)

This project demonstrates how to develop an ERC20 Token smart contract and its presale smart contract for an Initial Coin Offering deployed on BSC (but it's applicable for any Ethereum-based blockchain as Polygon).

## How it must be deployed

The first SC that must be deployed is Token.sol.

TokenPresale.sol SC must be deployed (by passing ERC20 Token smart contract address in the constructor) right after Token.sol is deployed.

If you decide to deploy both SC at once, it is done automatically by Truffle.

## How it works

Once both SC are deployed, 

NOTICE: Token.sol doesn't work on localhost, so if you need to do some testings, it should be deployed on the testnet.

## Token.sol

This smart contract allows to create and manage an ERC20 Token. It has the following features:

*   It can swap BNB for TKN.
*   It allows the owner to pause tokens transfers if necessary.

Once it receives funds from the presale contract, call addLiquidityToPS() to add TKNs liquidity to PancakeSwap.
