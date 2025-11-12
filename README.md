# DNS Allowlist for Technitium

This repository contains a small DNS allowlist (allowlist/whitelist) formatted for easy use with Technitium DNS Server or other DNS filtering software that accepts plain domain lists.

Purpose
- Provide a plain-text domain list of allowed domains.
- Support wildcard entries (use leading `*.` for subdomains).
- Serve raw files via GitHub raw URLs so you can point Technitium at the raw URL.

Usage with Technitium DNS Server
1. In the Technitium DNS Server web UI, go to the filtering / blocklist / whitelist area.
2. Add a new list and point it to the raw GitHub URL of the file. For example:
   https://raw.githubusercontent.com/Dfintz/dns-allowlist/main/wildcard/technitium-allowlist.txt
3. Set the list type to whitelist/allowlist or import the domains into Technitium's whitelist feature.
4. Technitium will fetch the latest version from the raw URL on its configured refresh schedule.

File format
- One domain per line.
- Lines starting with `#` are comments and ignored.
- Wildcard example: `*.example.com` will match subdomains such as `api.example.com`.

License
- MIT License (see LICENSE file)

Contributions
- Open issues or PRs to propose additions or changes to the list.