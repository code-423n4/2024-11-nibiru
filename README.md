# Nibiru audit details

- Total Prize Pool: $70,000 in USDC
  - HM awards: $55,800 in USDC
  - QA awards: $2,300 in USDC
  - Judge awards: $6,800 in USDC
  - Validator awards: $4,600 USDC
  - Scout awards: $500 in USDC
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts November 11, 2024 20:00 UTC
- Ends November 25, 2024 20:00 UTC

## Automated Findings / Publicly Known Issues

_Note for C4 wardens: Anything included in this `Automated Findings / Publicly Known Issues` section is considered a publicly known issue and is ineligible for awards._

- <https://github.com/NibiruChain/nibiru/issues/2075> - [evm] Oracle precompile UX would be improved by update time information S-triage

- <https://github.com/NibiruChain/nibiru/issues/2063> - A known issue we're in the progress of implementing a solution for. This doesn't present a security issue because transaction messages that use an invalid ERC20 in their FunToken mapping will simply fail to be executed.

# Overview

**Nibiru Chain** is a breakthrough Layer 1 blockchain and smart contract ecosystem providing superior throughput, improved security, and a high-performance EVM execution layer. Nibiru aims to be the most developer-friendly and user-friendly smart contract ecosystem, leading the charge toward mainstream Web3 adoption by innovating at each layer of the stack: dApp development, scalable blockchain data indexing, consensus optimizations, a comprehensive developer toolkit, and composability across multiple VMs.

## Links

- **Previous audits:**  We did a C4 Zenith audit right before this competitive audit, though it doesn't have a report I can link yet. A much earlier version of the chain was also audited by Zellic prior to Nibiru's inclusion of the EVM (<https://reports.zellic.io/publications/nibiru>).
- **Documentation:** :
  - [Docs | Nibiru Chain](https://nibiru.fi/docs/): Conceptual and technical documentation can be found here.
  - [Complete Golang reference docs](https://pkg.go.dev/github.com/NibiruChain/nibiru): (`pkg.go.dev`) For the blockchain implementation .
  - [Nibiru Modules](https://nibiru.fi/docs/dev/x/): Module-specific documentation
- **Website:**  <https://nibiru.fi/>
- **X/Twitter:**  <https://twitter.com/NibiruChain>
- **Discord:**  <https://discord.com/invite/HFvbn7Wtud>

---

# Scope

_See [scope.txt](https://github.com/code-423n4/2024-11-nibiru/blob/main/scope.txt)_

### Files in scope

File                                                |       code
----------------------------------------------------|-----------
x/evm/keeper/grpc_query.go                          |        565
x/evm/keeper/msg_server.go                          |        494
x/evm/statedb/statedb.go                            |        383
eth/rpc/backend/blocks.go                           |        373
x/evm/precompile/funtoken.go                        |        373
eth/rpc/backend/tx_info.go                          |        352
eth/rpc/rpcapi/eth_api.go                           |        305
eth/rpc/backend/call_tx.go                          |        258
x/evm/precompile/wasm.go                            |        243
eth/rpc/backend/utils.go                            |        230
eth/rpc/backend/tracing.go                          |        204
x/evm/precompile/wasm_parse.go                      |        198
x/evm/statedb/journal.go                            |        185
x/evm/statedb/state_object.go                       |        185
x/evm/keeper/erc20.go                               |        175
eth/rpc/backend/account_info.go                     |        170
x/evm/keeper/statedb.go                             |        152
x/evm/keeper/evm_state.go                           |        139
x/evm/keeper/gas_fees.go                            |        138
eth/rpc/backend/chain_info.go                       |        137
x/evm/precompile/precompile.go                      |        136
x/evm/keeper/bank_extension.go                      |        135
app/evmante/evmante_validate_basic.go               |        119
x/evm/keeper/funtoken_from_erc20.go                 |        118
app/evmante/evmante_gas_consume.go                  |        109
x/evm/keeper/keeper.go                              |        102
x/evm/keeper/call_contract.go                       |         96
x/evm/precompile/oracle.go                          |         92
app/evmante/evmante_can_transfer.go                 |         74
x/evm/keeper/vm_config.go                           |         72
x/evm/statedb/access_list.go                        |         65
x/evm/keeper/funtoken_from_coin.go                  |         64
eth/rpc/backend/node_info.go                        |         60
x/evm/keeper/funtoken_state.go                      |         60
app/evmante/evmante_increment_sender_seq.go         |         58
app/evmante/evmante_verify_eth_acc.go               |         57
app/evmante/evmante_mempool_fees.go                 |         56
app/evmante/evmante_sigverify.go                    |         53
eth/rpc/backend/backend.go                          |         46
x/evm/precompile/errors.go                          |         45
app/evmante/evmante_emit_event.go                   |         39
app/evmante/evmante_setup_ctx.go                    |         35
x/evm/statedb/config.go                             |         27
x/evm/statedb/debug.go                              |         24
x/evm/keeper/precompiles.go                         |         22
app/evmante/evmante_handler.go                      |         21
x/evm/keeper/msg_update_params.go                   |         21
x/evm/statedb/interfaces.go                         |         19
x/evm/keeper/hooks.go                               |         17
app/evmante/interfaces.go                           |          9
SUM:                                                |       7110

**Main Scope**| 
--
x/evm/keeper
x/evm/precompile
x/evm/statedb
app/evmante
eth/rpcapi/eth_api.go
eth/rpc/backend

**Ignore *.pb.go protobuf files**

**Important Tests**| 
--
evm-e2e
x/evm/evmtest

### Files out of scope

_See the files in [out_of_scope.txt](https://github.com/code-423n4/2024-11-nibiru/blob/main/out_of_scope.txt)_

## Scoping Q &amp; A

### General questions

| Question                                | Answer                       |
| --------------------------------------- | ---------------------------- |
| ERC20 used by the protocol              |       Any (all possible ERC20s)            |
| ERC721 used  by the protocol            |           N/A            |
| ERC777 used by the protocol             |           N/A             |
| ERC1155 used by the protocol            |           N/A            |
| Chains the protocol will be deployed on | Nibiru  |

### ERC20 token behaviors in scope

| Question                                                                                                                                                   | Answer |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [Missing return values](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#missing-return-values)                                                      |   In scope  |
| [Fee on transfer](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#fee-on-transfer)                                                                  |  In scope  |
| [Balance changes outside of transfers](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#balance-modifications-outside-of-transfers-rebasingairdrops) | In scope    |
| [Upgradeability](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#upgradable-tokens)                                                                 |   In scope  |
| [Flash minting](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#flash-mintable-tokens)                                                              | In scope    |
| [Pausability](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#pausable-tokens)                                                                      | In scope    |
| [Approval race protections](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#approval-race-protections)                                              | In scope    |
| [Revert on approval to zero address](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-approval-to-zero-address)                            | Out of scope    |
| [Revert on zero value approvals](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-zero-value-approvals)                                    | Out of scope    |
| [Revert on zero value transfers](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-zero-value-transfers)                                    | Out of scope    |
| [Revert on transfer to the zero address](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-transfer-to-the-zero-address)                    | Out of scope    |
| [Revert on large approvals and/or transfers](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-large-approvals--transfers)                  | In scope    |
| [Doesn't revert on failure](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#no-revert-on-failure)                                                   |  In scope   |
| [Multiple token addresses](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#revert-on-zero-value-transfers)                                          | Out of scope    |
| [Low decimals ( < 6)](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#low-decimals)                                                                 |   In scope  |
| [High decimals ( > 18)](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#high-decimals)                                                              | In scope    |
| [Blocklists](https://github.com/d-xo/weird-erc20?tab=readme-ov-file#tokens-with-blocklists)                                                                | Out of scope    |

### External integrations (e.g., Uniswap) behavior in scope

| Question                                                  | Answer |
| --------------------------------------------------------- | ------ |
| Enabling/disabling fees (e.g. Blur disables/enables fees) | No   |
| Pausability (e.g. Uniswap pool gets paused)               |  No   |
| Upgradeability (e.g. Uniswap gets upgraded)               |   Yes  |

### EIP compliance checklist

| Question                                | Answer                       |
| --------------------------------------- | ---------------------------- |
| x/evm/embeds/contracts/ERC20Minter.sol                  | Must be a valid, ownable ERC20. We're importing from OpenZeppelin and don't expect there to be issues based on the test suite.          |
| Contracts registered with a FunToken mapping to a Bank Coin on Nibiru                         | Must be valid ERC20s                 |

# Additional context

## Main invariants

1. NIBI is "ether" on the network, and microNIBI (written "unibi") is the smallest unit of NIBI. The following invariant holds true: 1 NIBI == 10^{18} wei == 10^{6} unibi. Note that this implies we cannot transfer values smaller than 10^{12} wei.

2. All of the standard invariants of the EVM StateDB should work exactly as they do on Ethereum mainnet.

3. Account state is not held by a particular VM, since an address is actually just a byte array. Thus, all accounts have both a nibi-prefixed Bech32 address and Ethereum hexadecimal address, each derived from the same bytes.

3. Any bank coin on Nibiru can be used to create a canonical ERC20 representation, for which the EVM itself (the module account) will be the owner.

4. Similar to (3), any ERC20 on Nibiru can be used to create a canonical bank coin representation. The owner of the ERC20 is unbounded, while only the EVM Module account can mint the bank coin representation produced.  

## Attack ideas (where to focus for bugs)

- When users of Nibiru interact over external clients like ethers.js and wagmi, is the behavior familiar like what developers would expect on the Ethereum L1 or networks like BSC, Base, or Arbitrum?
- Does the Ethereum JSON-RPC interface for Nibiru operate as expected in terms of transaction receipts, contract deployment and interactions, and how error messages are  displayed?

## All trusted roles in the protocol

Nibiru EVM has a few cases of special permissions: the EVM Module, the proof of stake governance authority, and the owner of an ERC20 as it pertains to the FunToken mapping mechanism:

| Role                                | Description                       |
| --------------------------------------- | ---------------------------- |
| EVM Module                          |- In the content of the FunToken mapping mechanism, the EVM itself is a Module Account with the sole authority to call `burnFromAuthority` from the `evm/embeds/contracts/ERC20Minter.sol` contracts that get deployed to represent Bank Coins as ERC20s.<br>- When a bank coin is created via “createFunTokenFromERC20”, the EVM Module is the only authority able to mint that coin.         |
| Governance Authority                             | A governance proposal can be submitted to update the EVM module parameters, such as the “CreateFunTokenFee”.                    |
|Wasm Precompile                          | When interacting with the Wasm VM from inside the EVM, the sender of the Wasm transaction message must be the sender of the EVM transaction message (the transaction signer). This allows us to cleanly compose the two VMs without complicating security checks.               |

## Describe any novel or unique curve logic or mathematical models implemented in the contracts

N/A

## Running tests

To run the local network, please install the [Nibiru CLI](https://nibiru.fi/docs/dev/cli/nibid-binary.html):

```bash
git clone --recurse https://github.com/code-423n4/2024-11-nibiru.git
cd 2024-11-nibiru

cargo install just
just # see all commands

just install
just build
just localnet # Run a local network

cd evm-e2e
cp .env_sample .env
just install
just test # Runs the EVM end to end tests suite with ethers.js
```

## Miscellaneous

Employees of Nibiru and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.
