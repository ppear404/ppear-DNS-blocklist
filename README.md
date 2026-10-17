# ppear-DNS-blocklist

DNS blocklist to supplement domain blocking.

This repository contains a simple, minimal DNS blocklist of domains intended to be used with local DNS-based blocking tools (Pi-hole, dnsmasq, Unbound, /etc/hosts, ad-blockers that accept a plain list of domains).

Usage

- hosts format: Add entries to `/etc/hosts` using `0.0.0.0 example.com` or `127.0.0.1 example.com`.
- domain-per-line: Use the plain list (one domain per line) with Pi-hole, dnsmasq, or ad-blockers that accept a domain list.
- dnsmasq/pihole: Drop the domain-per-line file into your blocklist configuration or use a URL to fetch the list.

Example

Contents (domain-per-line):

```
example.com
badtracker.example
ads.example.net
```

How to contribute

- Open an issue to suggest additions or removals.
- Send a pull request that updates the list. Keep each domain on its own line and avoid comments inside the domain list files.

Automate updates

If you host this list on a raw URL (GitHub raw), you can configure your DNS blocker to fetch it periodically so updates are applied automatically.

License

This repository is provided as-is. Use at your own risk. If you'd like a formal license, add a LICENSE file (MIT or similar is common).
