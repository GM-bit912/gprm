# Security Policy

## Report privately

Do not open a public issue for:

- an exposed credential, passphrase, token, private key, or client record;
- readable GPRM or FM-OPS source in a public artifact;
- an authentication or access-control weakness;
- protected model data or operational material found in public history.

Use the private business security contact configured by Fortis Minerva. Until
that contact is published and tested, contact the repository owner privately
through the existing verified channel.

Do not include live secrets or client data in the report. Identify the affected
file, URL, commit, and approximate time only.

## Supported public release

The intended supported product line is **GPRM v1.8.1 Founder Edition**. A
public encrypted gateway is supported only when its manifest identifies the
verified source release and its checksum has passed the release gate.

## Security boundary

Encryption of a static browser application protects the distributed file at
rest; it is not revocable account-based access. FM-OPS remains a separate,
restricted module and should move behind the server `/ops` role gate when that
deployment is ready.

## If exposure is suspected

1. Stop publishing and preserve evidence.
2. Revoke or rotate the affected secret immediately.
3. Review repository history, releases, Actions artifacts, Pages output, apps,
   deploy keys, webhooks, sessions, and tokens.
4. Reissue affected encrypted artifacts with new keys.
5. Record the incident and correction; never rely on deletion alone.
