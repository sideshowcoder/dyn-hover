Dyn DNS for Hover on OpenWRT
============================

Extracted and slightly modified based on the
[gist](https://gist.github.com/dankrause/5585907)

Setup on OpenWRT
----------------

1. Install Curl `$ opkg update && opkg install curl`
2. Move script to `/usr/bin/dyn-hover.sh`
3. Setup a scheduled task as
```
*/5 * * * * /usr/bin/dyn-hover.sh USERNAME PASSWORD DNSID
```

This will update your DNS record every 5 min to reflect the current external IP.


FAQ
---
1. find your DNS ID here: `https://www.hover.com/api/domains/yourdomain.com/dns/`
where `yourdomain.com` is the domain you want to set. The ID looks like: `dns1234567`.
