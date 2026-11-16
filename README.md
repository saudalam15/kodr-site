# kodr-site

Landing page for **Kodr**, an AI coding agent for any LLM.

- Production URL: **https://getkodr.ai** (custom domain, see below)
- Current URL until the domain is connected: https://saudalam15.github.io/kodr-site/
- Hosting: GitHub Pages, from `main` at the repo root (`index.html`, no build step)

## Connecting getkodr.ai

1. Register `getkodr.ai` in your own name (Cloudflare Registrar or Porkbun). Turn on auto-renew, 2FA, transfer lock and WHOIS privacy.
2. Verify the domain in GitHub: Settings → Pages → Verified domains → add `getkodr.ai`, then add the TXT record GitHub shows.
3. DNS records at the registrar:

   | Type  | Name | Value |
   |-------|------|-------|
   | A     | @    | 185.199.108.153 |
   | A     | @    | 185.199.109.153 |
   | A     | @    | 185.199.110.153 |
   | A     | @    | 185.199.111.153 |
   | AAAA  | @    | 2606:50c0:8000::153 |
   | AAAA  | @    | 2606:50c0:8001::153 |
   | AAAA  | @    | 2606:50c0:8002::153 |
   | AAAA  | @    | 2606:50c0:8003::153 |
   | CNAME | www  | saudalam15.github.io |

   On Cloudflare DNS, set these records to "DNS only" (grey cloud) until GitHub has issued the HTTPS certificate.
4. Add a `CNAME` file containing `getkodr.ai` to this repo (or set Custom domain in Settings → Pages), then tick **Enforce HTTPS**.

Do step 4 only after DNS is in place. Otherwise the github.io URL redirects to a domain that does not resolve yet.
