# buy uk proxies: what to check before you pay, and how per-IP billing changes the maths on British IPs

Search "buy UK proxies" and you'll get a wall of nearly identical pages promising 2 million, 20 million or 80 million British residential IPs, all with a benchmark graph. The genuinely useful question is narrower: what billing model does the job you have in mind actually fit, and what does a UK address cost under that model?

That's what this piece works through. It also covers one provider — 9Proxy — in enough detail to judge whether it's the right shape for your workload, including its full current price list, the UK targeting syntax from its own documentation, and the limits that show up once you're past the marketing layer.

## What "UK proxy" means depends on which of these you want

Most buyers conflate four different products. They aren't interchangeable, and the price gaps between them are large.

- **Rotating residential** — traffic exits through real UK household connections, and the IP usually changes per request or per session. Billed by gigabyte almost everywhere.
- **ISP / static residential** — an IP registered to a British ISP (BT, Virgin Media, Sky and so on) but served from a datacentre, so it's fast and it stays the same address for as long as you renew. Billed per IP per month.
- **Mobile** — 4G/5G addresses inside a UK carrier's network range, which is why platforms treat them as ordinary consumer traffic. The most expensive tier; typically billed per GB.
- **Datacentre** — cheap and fast, but in hosting ranges, so British retail and finance sites tend to spot them quickly.

For most UK jobs that need to look local — rank checking, price scraping, ad verification, account work — rotating residential or ISP is the right bracket. Published UK rates in the market currently run from roughly $1 to $4 per GB for rotating residential, and from about $2.50 per IP per month for static ISP addresses once you're buying in volume. Datacentre and mobile sit at the two extremes.

## Three numbers decide what you actually pay

**1. Per-GB or per-IP.** With per-GB billing the meter runs whenever data moves, so a page-heavy scraping run on a site full of images costs far more than the request count suggests. With per-IP billing you're paying for access, and traffic in many providers' models is unlimited while the IP is live.

**2. How long an IP stays alive.** Residential addresses are real people's connections. They go offline. If your workflow needs a session to survive for six hours — a checkout flow, a logged-in dashboard, a long crawl — average IP lifespan matters more than the headline per-IP price.

**3. How precisely you can target.** "UK" is not always enough. Price checks by city, regional SERP differences and listing sites vary enough by postcode that country-only targeting quietly produces wrong data. City, state, ZIP and ISP filters are the difference between usable and decorative.

## Why UK specifically, and where country-level access breaks down

The UK is one of Europe's more thoroughly geo-gated markets, and the gating is enforced by IP geography rather than login.

Property portals like Rightmove and Zoopla, retail pricing on Argos, Currys, John Lewis, Tesco and ASOS, job data on Indeed UK and Reed, and ad delivery checks across Sky, ITV and Channel 4 all serve different content — or no content — depending on where the request appears to come from. Google's UK results are their own thing too, which is why anyone tracking `.co.uk` rankings wants a British exit IP rather than a UK language setting on a US address.

A datacentre IP in London often isn't enough for that last group of sites. What those platforms score is the network profile behind the address: consumer ISP range, normal history, plausible geolocation.

## Where 9Proxy fits a UK job

9Proxy is a residential proxy provider selling into 90+ locations with an advertised pool of 20M+ IPs, supporting HTTP/HTTPS and SOCKS5. The United Kingdom is in its supported country list, and it appears in the vendor's own examples — the Linux documentation literally uses `-c UK` to demonstrate forwarding a British IP to a port.

What's relevant to a UK purchase is the targeting granularity and the billing structure:

- Country, state, city, ZIP code and ISP filters on both product lines
- For GB-based plans, targeting sits in the proxy username, so you can change it per request without opening a dashboard: `subuser-country-gb` for a rotating British IP, `-city-london` to narrow it, `-sst-15` to hold one for 15 minutes
- IP-based plans are billed per address with unlimited traffic while that address is live, and unused IPs sit in your balance without expiring
- Live British IPs last anywhere from a few hours to roughly 24 hours, which is normal for residential pools
- Two mechanisms soften that: proxies from the last 24 hours can be reused free through the Today List, and proxies that die quickly can be reported for replacement

There's one structural catch worth knowing before you buy. The IP-based model routes through a desktop app that forwards proxies to local ports — Windows, macOS and Linux only. The GB-based model works straight from the dashboard with username/password or IP whitelisting, no app. If you're deploying on a server or onto a phone, that difference decides which product you buy.

👉 [Open a 9Proxy account and check live UK availability](https://bit.ly/9-Proxy)

## The full current price list

9Proxy raised prices on 1 June 2026 for its IP-based and bundle packages, its first adjustment since launch; GB-based packages were left unchanged. The table below is the published list across all four product groups.

| Package | What you get | Price | Billing model | Buy |
| --- | --- | --- | --- | --- |
| 100 IPs | 100 residential IPs | $24 ($0.24/IP) | Pay per IP, unused IPs don't expire | [Get 100 IPs](https://bit.ly/9-Proxy) |
| 500 IPs | 500 residential IPs | $72 ($0.144/IP) | Pay per IP | [Get 500 IPs](https://bit.ly/9-Proxy) |
| 1,000 + 500 IPs | 1,500 residential IPs | $126 ($0.084/IP) | Pay per IP, 500 bonus IPs | [Get 1,500 IPs](https://bit.ly/9-Proxy) |
| 2,500 IPs | 2,500 residential IPs | $210 ($0.084/IP) | Pay per IP | [Get 2,500 IPs](https://bit.ly/9-Proxy) |
| 5,000 IPs | 5,000 residential IPs | $360 ($0.072/IP) | Pay per IP | [Get 5,000 IPs](https://bit.ly/9-Proxy) |
| 15,000 IPs | 15,000 residential IPs | $720 ($0.048/IP) | Pay per IP | [Get 15,000 IPs](https://bit.ly/9-Proxy) |
| 25,000 IPs | 25,000 residential IPs | $863 ($0.035/IP) | Pay per IP | [Get 25,000 IPs](https://bit.ly/9-Proxy) |
| 50,000 IPs | 50,000 residential IPs | $1,438 ($0.029/IP) | Pay per IP | [Get 50,000 IPs](https://bit.ly/9-Proxy) |
| Business 100,000 IPs | 100,000 residential IPs | $2,300 ($0.023/IP) | Pay per IP, business tier | [Get 100,000 IPs](https://bit.ly/9-Proxy) |
| Business 200,000 IPs | 200,000 residential IPs | $4,140 ($0.021/IP) | Pay per IP, business tier | [Get 200,000 IPs](https://bit.ly/9-Proxy) |
| Business 500,000 IPs | 500,000 residential IPs | $8,625 ($0.018/IP) | Pay per IP, business tier | [Get 500,000 IPs](https://bit.ly/9-Proxy) |
| GB Starter | 5 GB of traffic | $15 ($3.00/GB) | Pay per GB, 180-day validity | [Get 5 GB](https://bit.ly/9-Proxy) |
| GB 50 + 5 | 55 GB of traffic | $105 ($2.10/GB) | Pay per GB, 180-day validity | [Get 55 GB](https://bit.ly/9-Proxy) |
| GB 100 | 100 GB of traffic | $150 ($1.50/GB) | Pay per GB, 180-day validity | [Get 100 GB](https://bit.ly/9-Proxy) |
| GB 200 | 200 GB of traffic | $200 ($1.00/GB) | Pay per GB, 180-day validity | [Get 200 GB](https://bit.ly/9-Proxy) |
| GB 1,000 | 1,000 GB of traffic | $800 ($0.80/GB) | Pay per GB, 180-day validity | [Get 1,000 GB](https://bit.ly/9-Proxy) |
| GB 2,000 | 2,000 GB of traffic | $1,500 ($0.75/GB) | Pay per GB, 180-day validity | [Get 2,000 GB](https://bit.ly/9-Proxy) |
| Enterprise GB 3,000 | 3,000 GB of traffic | $2,160 ($0.72/GB) | Pay per GB, no expiry | [Get 3,000 GB](https://bit.ly/9-Proxy) |
| Enterprise GB 6,000 | 6,000 GB of traffic | $4,200 ($0.70/GB) | Pay per GB, no expiry | [Get 6,000 GB](https://bit.ly/9-Proxy) |
| Enterprise GB 10,000 | 10,000 GB of traffic | $6,800 ($0.68/GB) | Pay per GB, no expiry | [Get 10,000 GB](https://bit.ly/9-Proxy) |
| Bundle Starter | 100 IPs + 5 GB | $30 | Mixed, traffic valid 180 days | [Get the Starter bundle](https://bit.ly/9-Proxy) |
| Bundle Popular | 1,500 IPs + 50 GB | $180 | Mixed, traffic valid 180 days | [Get the Popular bundle](https://bit.ly/9-Proxy) |
| Bundle Pro | 5,000 IPs + 500 GB | $720 | Mixed, traffic valid 180 days | [Get the Pro bundle](https://bit.ly/9-Proxy) |

A few things the table makes obvious. The entry point is 100 IPs at $24 — there's no single-IP option on the official site, so a one-off UK test costs that much at minimum. The per-IP price falls by more than 90% between the smallest and largest tier. And the GB line is the only one that didn't move in June 2026, which makes the larger GB tiers relatively better value than they were a year ago.

Prices move, so check the number at checkout before you commit to a volume tier.

## Which plan fits which UK job

**A handful of UK accounts, checked daily.** The 100-IP tier. Each address lives hours to a day, and the Today List lets you reuse one that comes back within 24 hours without paying again. If you're running a UK social or marketplace account through an antidetect browser, this is the cheap end that still gives you distinct British addresses.

**Ongoing scraping with heavy rotation.** GB-based. You generate as many endpoints as your balance allows and rotate freely — the model matches jobs where each request uses little data and every request should look like it came from a different household. With 200 GB at $1.00/GB, a scraper pulling mostly text can cover a very large number of page fetches before the balance runs out. The 180-day validity matters here: project-based UK work runs unevenly, and traffic doesn't evaporate between sprints.

**Mixed workload — stable IPs for logins plus rotation for collection.** A bundle. The Popular tier at $180 gives 1,500 IPs alongside 50 GB, which is the combination most agencies end up needing: persistent addresses glued to specific accounts, and a rotating UK pool for everything else.

**Continuous infrastructure.** Enterprise GB tiers, where validity is unlimited and the per-GB rate bottoms out at $0.68. That's the tier that makes sense if you'd otherwise be rebuying UK bandwidth every six months.

👉 [See the full 9Proxy pricing page and pick a UK package](https://bit.ly/9-Proxy)

## Getting a UK IP running

With an IP-based package: sign up, buy the tier, then install the desktop app for Windows, macOS or Linux. Inside it, filter by country to the UK — you can add state, city, ZIP or ISP — select an address and forward it to a local port. You then point your browser or automation tool at `127.0.0.1:port`. There's a command-line shortcut for headless setups:


9proxy proxy -c UK -p 60000


That forwards a UK residential proxy to port 60000. If you've used a proxy in the last 24 hours, the `-n` flag pulls from the Today List and doesn't spend another IP.

With a GB-based package, there's nothing to install. Log into the dashboard, open Residential Proxies by GB, click Get Proxy, and generate credentials using either a sub-user or whitelisted server IP. Then build the username:

- `subuser-country-gb` — rotating British IPs, a fresh one per request
- `subuser-country-gb-city-london` — narrowed to one city
- `subuser-country-gb-city-london-sst-15` — sticky, holding one address for 15 minutes
- add `-ssid-id1`, `-ssid-id2` and so on if you need several parallel sticky sessions from the same configuration

One warning from 9Proxy's own docs applies directly to UK work: combining state, city and ISP filters all at once shrinks the available pool, and you may get fewer usable addresses than you'd expect. Target country plus one extra filter unless the job genuinely requires the precision.

## Limits to weigh before you buy

**Sticky sessions are measured in minutes, not weeks.** GB-based sticky mode holds an address for the session time you set, and IP-based addresses live hours to about a day. If your UK use case is a permanently logged-in account on one unchanging IP — a seller dashboard, for example — you want a static ISP address from a provider that sells one, not a residential pool. This is a real gap in the product line, not a detail you can configure around.

**Streaming is hit and miss.** One published review found 9Proxy effective on retail sites but occasionally detected on Netflix. If your demand for a UK IP is BBC iPlayer or a streaming service, test on the entry tier before committing to volume.

**The IP-based model needs the app.** No app, no proxies on that plan. Teams running containerised UK scrapers should start with GB-based.

**Third-party reviews are thin.** Ratings circulating on directory sites sit around 3.9 and one independent review puts uptime near 99% for scraping and account work. That's a small sample compared with the long-established UK proxy vendors, so treat the reputation as unproven at scale.

## Questions that come up before a first UK purchase

**Do unused UK IPs expire?** On IP-based plans, no — the balance sits there until you forward an address. GB packages carry a 180-day validity window, and the enterprise tiers remove that limit.

**What payment methods are accepted?** The vendor lists cards, major cryptocurrencies including USDT, BTC, ETH and others, plus Apple Pay, Google Pay and Alipay.

**Is there a UK-specific plan?** No. Country targeting is included on every package, and UK IPs are priced the same as any other location — the price depends on how many IPs or how much bandwidth you buy, not on which country you point them at.

**Is there a free trial?** Trials have been offered to new users periodically and depend on availability; the reliable route is to ask support whether one is open and whether you want it IP-based or GB-based.

**Can a team share one account?** Yes — sub-accounts and share codes are built in, which matters if several people need separate UK proxies from one balance.

## The short version

If you're buying UK proxies for account work, use the IP-based model so each account gets its own British address, and start at $24 for 100 IPs. If you're collecting data at volume, buy GB — $1.00/GB at the 200 GB tier or $0.68/GB at enterprise, with rotation on every request. Mixing both, take a bundle. And if you need one fixed British IP that never changes, accept that you're shopping for ISP proxies elsewhere rather than trying to force a rotating residential pool into that job.

👉 [Buy UK proxies from 9Proxy and start with a plan that matches your workload](https://bit.ly/9-Proxy)
