# Uniswap V2

[![Actions Status](https://github.com/VenomProtocol/venomswap-core/workflows/CI/badge.svg)](https://github.com/VenomProtocol/venomswap-core/actions)
[![Version](https://img.shields.io/npm/v/@venomswap/core)](https://www.npmjs.com/package/@venomswap/core)

In-depth documentation on Uniswap V2 is available at [uniswap.org](https://uniswap.org/docs).

The built contract artifacts can be browsed via [unpkg.com](https://unpkg.com/browse/@venomswap/core@latest/).

# Local Development

The following assumes the use of `node@>=10`.

## Install Dependencies

`yarn`

## Compile Contracts

`yarn compile`

## Run Tests

`yarn test`

## Verify

1. `yarn`
2. `yarn compile`
3. compare `bytecode` from `build/UniswapV2Factory.json` with [Contract Creation Code](https://www.smartscan.cash/transaction/0xf9406b2def8cf0bdd68c99816b532de0b77143a100cb9c39e2de106a221f8c35)
4. get ABI-encoded constructor args and append to compiled bytecode for completeness https://abi.hashex.org/

Factory: `0xDd749813a4561100bDD3F50079a07110d148EaF5`
Deployment artifact: https://github.com/smartdogebch/smartswap-dex-contracts/blob/master/deployments/Factory.json

Note: compile on Windows or Truffle will produce differing compiled bytecode for metadata