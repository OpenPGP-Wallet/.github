# OpenPGP Wallet

A non-custodial, multi-network crypto wallet for the desktop with **no seed phrase to write down**. The master key
is protected by OpenPGP and a 2-of-3 Shamir backup kit, instead of 12 or 24 words on a piece of paper.

- **One master key, 19 networks**: Bitcoin, Ethereum and its L2s, Solana, Zcash (transparent and shielded),
  Monero, Cardano, XRP Ledger, Tezos and more.
- **The interface never sees a secret.** Everything that gets signed is rebuilt and checked in Rust, and every
  send goes through a native OS confirmation dialog.
- **Backups you can trust.** Each Shamir share goes to its own USB drive and is decrypted back before the app
  says the backup is done. Any two shares restore the wallet; one alone reveals nothing.
- **FROST threshold signing for shielded Zcash**, 2-of-3, in the wallet since v2.16: the computer signs
  together with a second device, over QR codes and with no server in the middle. The co-signer is a desktop
  tool for now ([frost-zec](https://github.com/OpenPGP-Wallet/frost-zec)); the phone app comes next.

> [!WARNING]
> **Pre-audit software.** OpenPGP Wallet works end to end, but it has not been reviewed by an independent
> auditor and the Windows binaries are not code-signed yet. Please don't use it with funds you can't afford to
> lose.

## Links

- [**openpgp-wallet**](https://github.com/OpenPGP-Wallet/openpgp-wallet): the desktop app, in Rust and Tauri
  (MIT license)
- [**frost-zec**](https://github.com/OpenPGP-Wallet/frost-zec): the FROST co-signing protocol for shielded
  Zcash, as a Rust library with its specification and a test co-signer (MIT license)
- [Website and video guides](https://khadevs.github.io/openpgp-wallet-site/)
- [FROST white paper](https://khadevs.github.io/openpgp-wallet-site/frost-white-paper.html)
- Found a security issue? Please report it privately, as described in the
  [security policy](https://github.com/OpenPGP-Wallet/openpgp-wallet/security/policy).
- Contact: openpgp-wallet@protonmail.com
