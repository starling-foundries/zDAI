# Overview

This is a repository to collect resources and plan an implementation of a bridge between Ethereum and Zilliqa for the express purpose of bringing ETH-native DAI stablecoins (and potentially others) to interact with ZIL smart contracts. 

## Project Status

This is an early phase pre-POC discussion right now. Pull requests and discussions in the issue tracker are welcome.

## Prior Art

[xDAI](https://poa.network/xdai): A POA sidechain for DAI, DPOS consensus and the ability to pay transfer fees in xDAI make it attractive.
[EOS-21](https://github.com/sheos-org/eos21): A purely contract (plus an oracle) that 'teleports' ERC20 tokens to the EOS blockchain. Essentially it is a Solidity Contract that collects the token and EOS account info, which is watched by an oracle that notifies the EOS contract to issue a coordinated token on their platform. 
[COSMOS IBC](https://cosmos.network/docs/spec/ibc/): An inter-blockchain communication protocol. Works on arbitrary tokens and most DLTs with verifiable finality and merkle proofs. Would entail creating a bridge Tendermint POS chain and require a two-way peg to bridge ETH to ZIL.


## Relationship to metatransactions

If EOS-21 is a model, the metatransactions functionality that is delivered in phase 0 (ERC777 with operator) can replicate xDAI's pay-fee-with-token feature. This could also pay for maintenance of the project if the tokenfee is greater than the cost of the invoked scilla transitions. 
