# Fortis Minerva — Public Distribution Repository

This repository is the public shopfront and ciphertext-only distribution
boundary for **GPRM v1.8.1 Founder Edition**.

## What may be public

- the approved public website and browser-only demo;
- the public verification annex and capability booklet;
- independently encrypted `platform.html` and `ops.html` gateways;
- release manifests, checksums, and public validation policy.

## What must never be public

- readable GPRM analyst-platform source;
- readable FM-OPS source or doctrine;
- fitted parameters, adjudicated episodes, or premium instances;
- passphrases, API keys, tokens, client data, operational logs, or personal
  information;
- internal release ZIPs, source maps, or server configuration.

The public method arithmetic is intentionally inspectable. Protected model
assets and premium content belong in the server-side data plane, not Git.

## Release status

This prepared repository is **not approved for publication yet**.

The live `ops.html` is a separate encrypted FM-OPS gateway and matches the
controlled v1.8.1 release byte-for-byte. The copied `platform.html` is the
current live encrypted gateway, but it predates the controlled v1.8.1 Founder
Edition build. It must be rebuilt locally from the verified v1.8.1 source with
the offline release tool before any release pull request is opened.

Never paste or send a decryption passphrase to an AI, issue, pull request,
workflow, or chat. Perform encryption locally on the authorised holder's
computer.

## Public demo integrity

The demo uses the v1.8.1 headline bands:

- `CRITICAL` at eta >= 2.15
- `WARNING` at 1.75 <= eta < 2.15
- `WATCH` at 1.30 <= eta < 1.75
- `CLEAR` below 1.30

It runs locally and has no API-key field or network write path. It is
illustrative decision support, not an operational system or validated
forecasting service.

## Release procedure

1. Resolve the GitHub account-security check and confirm authorised ownership.
2. Generate a fresh encrypted `platform.html` locally from the verified
   v1.8.1 source.
3. Run `node scripts/validate-public.mjs`.
4. Confirm the three private repositories and security rules are in place.
5. Open a reviewed pull request; do not push directly to `main`.
6. Deploy through a protected GitHub Pages environment with no decryption
   secrets in Actions.

The full control set is in the companion secure-split package.
