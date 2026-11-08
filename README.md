# DNSSEC Inspector

A free, single-page DNSSEC (Domain Name System Security Extensions) validator — check whether a domain's chain of trust is signed and valid, inspect its DS and DNSKEY records, and see exactly why validation failed if it did. Live at [dnssec.hbenali.ovh](https://dnssec.hbenali.ovh).

No backend, no build step, no dependencies — it's one static `index.html` calling a public API directly from the browser.

## Features

- **Validate** any domain's DNSSEC chain of trust via DNS-over-HTTPS, using the resolver's own `AD` (Authenticated Data) flag
- **DS & DNSKEY inspection** — key tags, algorithms, digest types, KSK/ZSK roles
- **Failure diagnosis** — surfaces the resolver's Extended DNS Error (RFC 8914) reason when validation fails (expired signature, missing DNSKEY, etc.)
- **Raw JSON viewer** for both DNS responses
- **Guide section** — DNSSEC overview, how validation works, common failure modes
- Dark editorial design with self-hosted fonts (see `fonts/`)
- Fully responsive and accessible

## Running locally

No build step required — just serve the directory:

```bash
python3 -m http.server 8080
```

## License

MIT
