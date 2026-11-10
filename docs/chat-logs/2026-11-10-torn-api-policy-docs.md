# Documentation work log: Torn API rule changes (2026-11-10)

**Owner request:** “Update documentation where it is needed with these new rules. Go through all my torn repos and make sure this is documented.”

## Source

- Torn forum announcement supplied as screenshots by the owner, dated November 10, 2026.
- Torn official API limits and cache reference: https://www.torn.com/api.html#limits and https://staticfiles.torn.com/api.html

## Recorded changes

- Global one-hour cache for `market/itemmarket`, `market/properties`, `market/rentals`, `company/companies`; five minutes for `torn/bounties` and `user/bounties`.
- `user/bazaar` now requires a key with at least Limited Access and can return only the key owner's own bazaar; insufficient access may return an empty array.
- The 100/minute player-wide API request cap across keys, 5,000/minute per-IP service limit, and prohibition on bypass through multiple servers/IPs.
- Restrictions against scraping / unauthorized automation and the distinction between global cache and ordinary service cache.
- No assumption that unrelated endpoints (including Auction House, personal item market and inventory) inherit the one-hour rule.

## Files documented in this repository

- `docs/TORN-API-2026-11-10.md`
- `README.md`

## Scope and verification limits

Documentation-only changes committed to GitHub. **No application or userscript code, API key, secret, service, cron schedule, live database, migration, collector, rate-limit implementation, or deployment changed.** This was not a runtime audit of live credentials or API responses. Existing historical project documentation is preserved and may refer to retired deployments or earlier architecture. Current rules can change; recheck Torn's official documentation before implementing new functionality.
