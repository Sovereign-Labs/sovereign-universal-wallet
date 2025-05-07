# Sovereign universal wallet

## Intro

This repository provides a "universal" wallet for interacting with all Sovereign SDK chains. See the generated rustdoc for more details.

## Getting Started

1. Add any needed dependencies to your `Cargo.toml`.

```
sov-universal-wallet = { git = "https://github.com/Sovereign-Labs/sovereign-universal-wallet.git", branch = "master" }
sov-universal-wallet-macros = { git = "https://github.com/Sovereign-Labs/sovereign-universal-wallet.git", branch = "master" }
sov-universal-wallet-macro-helpers = { git = "https://github.com/Sovereign-Labs/sovereign-universal-wallet.git", branch = "master" }
```

2. Import the needed crate. For example: `use sov_universal_wallet::schema::Schema;`

### What's Inside?

This repository provides crates with two main functions:

- `sov_universal_wallet::UniversalWallet`: a proc-macro deriving the SchemaGenerator trait that allows types (and subtypes) to be used to construct a Schema, and
- `sov_universal_wallet::Schema`: the actual Schema, constructed from a type deriving SchemaGenerator, that enables universal wallet functionality, namely human-readable display and serializing from JSON to borsh in any context without the original Rust types needing to be present.

The proc macro is re-exported from githe `schema` crate and its attributes are documented in the corresponding doc-comment.
