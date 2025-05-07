# Sovereign universal wallet
This repository provides crates with two main functions:
 * `sov_universal_wallet::UniversalWallet`: a proc-macro deriving the SchemaGenerator trait that allows types (and subtypes) to be used to construct a Schema, and
 * `sov_universal_wallet::Schema`: the actual Schema, constructed from a type deriving SchemaGenerator, that enables universal wallet functionality, namely human-readable display and serializing from JSON to borsh in any context without the original Rust types needing to be present.

The proc macro is re-exported from the `schema` crate and its attributes are documented in the corresponding doc-comment.
