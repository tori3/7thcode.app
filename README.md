# 7thcode Trust & Support

Dependency-free public pages for 7thcode Atlassian Marketplace apps.

## Published routes

- `https://trust.7thcode.app/`
- `https://trust.7thcode.app/support/`
- `https://trust.7thcode.app/security/`
- `https://trust.7thcode.app/privacy/`
- `https://trust.7thcode.app/terms/`

The complete site is under `docs/` so GitHub Pages can publish directly from
the `main` branch and `/docs` folder without a custom build workflow.

## GitHub Pages configuration

1. Open **Settings → Pages** in the repository.
2. Choose **Deploy from a branch**.
3. Select `main` and `/docs`, then save.
4. Set the custom domain to `trust.7thcode.app` and enable HTTPS after the certificate is ready.

## DNS

Create a DNS-only CNAME record from `trust` to `tori3.github.io`. Keep the apex
domain available for the main 7thcode site, keep the GitHub domain-verification
TXT record, and do not create wildcard records.

The exact current records are documented by GitHub:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Policy alignment sources

The common policy language is intentionally subordinate to the Marketplace
order and each product's more specific documentation. It was aligned against:

- Flow Guard [support](https://tori3.github.io/flow-guard-docs/support.html),
  [security](https://tori3.github.io/flow-guard-docs/security.html),
  [privacy](https://tori3.github.io/flow-guard-docs/privacy.html),
  [data controls](https://tori3.github.io/flow-guard-docs/data-controls.html), and
  [terms](https://tori3.github.io/flow-guard-docs/terms.html)
- StatusLens [security](https://github.com/tori3/statuslens-docs/blob/main/SECURITY.md)
  and [privacy](https://github.com/tori3/statuslens-docs/blob/main/PRIVACY.md)
- CloneGuard's current manifest and product, security, privacy, and release
  documentation in the parent repository

Before publication, the provider identity and liability language should receive
legal review for the actual Marketplace seller and customer jurisdictions.

## Verification record — 13 August 2026

- Confirmed the home, support, security, privacy, terms, stylesheet, social
  preview, and sitemap routes return HTTP 200 from a local static server.
- Confirmed no legacy contact address, superseded liability period, or
  unsupported service-language promise remains in the prepared trust site.
- Confirmed public DNS advertises Cloudflare mail-routing MX records and an SPF
  record for `7thcode.app`. A real inbound delivery test and forwarding-target
  check are still required before the address is published.
