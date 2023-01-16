![my badge](https://badgen.net/badge/license/MIT/green) ![my badge](https://badgen.net/badge/version/v0.0.1/green) ![my badge](https://badgen.net/badge/icon/v8.5.5/green?icon=npm&label) ![my badge](https://badgen.net/badge/nodejs/v16.15.0/green) ![my badge](https://badgen.net/badge/truffle/v5.5.9/green) ![my badge](https://badgen.net/badge/solidity-compiler/v0.8.13/green)

# Solidity ICO Presale Smart Contract

This project demonstrates how to develop an ERC20 Token smart contract and its presale smart contract for an Initial Coin Offering deployed on BSC (but it's applicable for any Ethereum-based blockchain as Polygon).

## How it must be deployed

The first SC that must be deployed is Token.sol.

TokenPresale.sol SC must be deployed (by passing ERC20 Token smart contract address in the constructor) right after Token.sol is deployed.

If you decide to deploy both SC at once, it is done automatically by Truffle.

## How it works

Once both SC are deployed, 

ℹ NOTICE: Token.sol doesn't work on localhost, so if you need to do some testings, it should be deployed on the testnet.

## Token.sol

This smart contract allows to create and manage an ERC20 Token. It has the following functions:

*   addLiquidityToPS(): allows to add liquidity to PancakeSwap.
*   approve(): allows the owner to approve any address to transfer tokens on your behalf.
*   approvePresaleContract(): approves presale SC to transfer initial tokens on your behalf.
*   burn(): allows to burn TKN tokens.
*   changeManager(): allows to change managers.
*   decreaseAllowance(): decreases the allowance for a given address.
*   disableTax(): disables taxes for tokens transactions.
*   enableTax(): enables taxes for tokens transactions.
*   exclude(): excludes addresses which will not pay taxes.
*   increaseAllowance(): increases the allowance for a given address.
*   pause(): allows to pause any transaction.
*   releaseTokens(): it allows to release those tokens that were stored from taxes.
*   removeExclude(): removes addresses from excluded to pay taxes.
*   renounceOwnership(): the owner renounces to the ownership of this SC.

*   It can swap BNB for TKN.
*   It allows the owner to pause tokens transfers if necessary.

Once it receives funds from the presale contract, call addLiquidityToPS() to add TKNs liquidity to PancakeSwap.

## TokenPresale.sol

This smart contract allows to manage the ICO for such ERC20 Token. It has the following features:

*   It can swap BNB for TKN.
