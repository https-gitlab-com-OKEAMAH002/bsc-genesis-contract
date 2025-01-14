# Changelog

## v1.0.0-beta.0

BUG FIXES
* [\#9](https://github.com/bnb-chain/bsc-genesis-contract/pull/9) Fix gov hub do not well handle when the target account is not contract

FEATURES
* [\#7](https://github.com/bnb-chain/bsc-genesis-contract/pull/7) Implement governance mechanism to update parameters in build-in system contract
* [\#12](https://github.com/bnb-chain/bsc-genesis-contract/pull/12) Implement token unbind mechanism
* [\#21](https://github.com/bnb-chain/bsc-genesis-contract/pull/21) Support miniToken cross chain transfer
* [\#28](https://github.com/bnb-chain/bsc-genesis-contract/pull/28) Add more events about token bind and transfer to facilitate reconciliation
* [\#29](https://github.com/bnb-chain/bsc-genesis-contract/pull/29) Implement a mechanism enable or disable channel through governance

IMPROVEMENTS
* [\#3](https://github.com/bnb-chain/bsc-genesis-contract/pull/3) Check sequence first to save gas for relayers
* [\#13](https://github.com/bnb-chain/bsc-genesis-contract/pull/13) Refactor cross chain architecture, communication layer: verify proof and manage sequence, application layer: focus on detailed application scenario
* [\#14](https://github.com/bnb-chain/bsc-genesis-contract/pull/14) Gov/Validator/Slash modification for refactor of cross chain mechanism
* [\#19](https://github.com/bnb-chain/bsc-genesis-contract/pull/19) Optimize rlp decoding and encoding library to save gas
* [\#22](https://github.com/bnb-chain/bsc-genesis-contract/pull/22) Add fail ack handler for transferOut
* [\#24](https://github.com/bnb-chain/bsc-genesis-contract/pull/24) Split tokenhub contract into tokenhub(for cross chain transfer) and tokenManager(for token bind and unbind)

# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]
- Placeholder for any new changes or features before the next release.

---

## [1.0.0] - 2025-01-14

### Added
- **Token Contract**: BOOM ($BM) with 18 decimals.
- **Ownership Control**: The deployer address is set as the initial owner.
- **Deposit/Withdraw Functions**: Allow users to deposit and withdraw BNB with event logging.
- **Emergency Withdraw**: The owner can withdraw all funds in case of emergency.
- **Transfer Functions**: Allow users to transfer tokens and approve transfers.
- **Fallback Function**: Support for direct BNB deposits.
- **Ownership Transfer**: Admin functionality to transfer ownership to a new address.

### Fixed
- **Reentrancy Protection**: Ensured safer withdrawals using `call{value:}` to mitigate reentrancy attacks.
- **Allowance System**: Approve and transferFrom functions ensure correct allowance checks.

---

## [0.9.0] - 2025-01-10

- **WBNB Contract**: Initial version based on Wrapped BNB (WBNB) contract structure.
- **Owner-Specific Access**: Deployer is set as the owner by default.

---

### Notes:
- The `Unreleased` section is for future changes. Update this section when new changes are made before a release.
- Be sure to update each section with the proper date and changes for future versions.
