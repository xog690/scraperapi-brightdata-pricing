# Bright Data Web Unlocker Alternative: What You'd Pay, Which Plan Fits, and What ScraperAPI Can't Replace

Bright Data's Web Unlocker charges $1.50 per 1,000 successful requests whether the page is a hard-to-scrape retailer or a plain public blog. That flat rate is the reason most teams start looking for an alternative, and it's also the reason a straight swap often overshoots. A standard page on ScraperAPI's Hobby plan works out to roughly **$0.49 per 1,000 requests** (calculated from the published $49 for 100,000 credits), about a third of the Web Unlocker rate. You can also keep Bright Data for the domains that genuinely need it and route the public share elsewhere, which is usually where the money is.

Below: the full ScraperAPI plan table, how its credit system turns one headline number into very different per-page costs, what it can and can't replace, and the Bright Data billing mechanics that make invoices climb.

> **Quick pick:** if most of your URLs are ordinary public pages and you bill monthly, start on **Hobby at $49/month** — 100,000 credits, 20 concurrent threads, a 7-day trial with 5,000 credits and no card. You're only charged for successful 200 and 404 responses. Keep Bright Data if you need its residential proxy pool, mobile proxies or ready-made dataset marketplace.
>
> 👉 [See ScraperAPI's plans and current credit pricing](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## ScraperAPI plans and prices

| Plan | Credits/month & concurrency | Price & billing | Get started |
| --- | --- | --- | --- |
| Free | 1,000 credits, 5 threads | $0, monthly | [Start on the free plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Hobby | 100,000 credits, 20 threads | $49/month | [Open Hobby at $49/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Advanced | 21,500,000 credits, 500 threads | $1,975/month | [Open Advanced at $1,975/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Enterprise | 22,000,000+ credits, 500+ threads | Custom quote | [See how to contact sales](https://www.scraperapi.com/pricing/?fp_ref=coupons) |

ScraperAPI's pricing page also lists Startup, Business, Scaling and Professional tiers between Hobby and Advanced, each with a larger credit allowance and thread count. Check the pricing page for their current numbers. Two limits matter more than the credit count: geotargeting is US and EU only on Hobby and Startup, and it goes global from Business upward. Pay-as-you-go overage is available from Scaling upward.

## Why Bright Data bills get bigger than the quote

Three mechanics explain most of the surprise.

**One rate for every page.** Web Unlocker is $1.50 per 1,000 successful requests on pay-as-you-go, $499/month for 383,000 requests on the Scale plan, then $1.30 per 1,000 after that, with 5,000 free requests a month. Rendering and CAPTCHA solving are included. A plain HTML page and a Cloudflare-protected product page cost the same, so the price you pay is set by your hardest target rather than the average of your list.

**Custom features flip failed requests onto the invoice.** Bright Data's documentation states that once you enable custom Web Unlocker features — your own headers, your own cookies, or a manual expect-element — requests are billed at 100% including failures. If a target fails 40% of the time, the effective cost per delivered page rises from $1.50 to about **$2.50 per 1,000**. Teams that switched on custom headers for one stubborn site often find the change spread across their whole bill.

**Premium domains.** Bright Data applies per-domain surcharges on top of the base rate and does not publish the rates. Assume any target that lands on that list costs more than the headline figure; you won't know by how much until the invoice arrives.

Bright Data's other products bill on different units: Web Scraper API at the same $1.50 per 1,000 records, Scraping Browser at $8 per GB (roughly $19.53 per 1,000 pages at 2.5 MB each), datasets from $250 per 100,000 records. Plans are monthly only, with a $10 minimum top-up below the committed tiers. None of that is unreasonable for a 400M+ residential IP network across 195 countries, 1,280 pre-built scrapers and unlimited concurrency. It is expensive if what you actually need is to read public pages.

## How ScraperAPI's credits translate into real per-page costs

A credit is not a page. ScraperAPI prices each request by what it has to do:

| Request type | Credits |
| --- | --- |
| Standard page | 1 |
| Amazon, Walmart, eBay | 5 |
| Google or Bing (including subdomains) | 25 |
| LinkedIn | 30 |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX, Akamai) | +10 |
| JavaScript rendering | +10 |
| Premium proxies | +10 |
| Ultra premium | 30 |
| Ultra premium + rendering | 75 |

The credit price itself changes with the plan. At Hobby, $49 buys 100,000 credits, which is $0.00049 each, or about **$0.49 per 1,000 credits**. At Advanced, $1,975 buys 21,500,000 credits, about $0.0000919 each, or roughly **$0.09 per 1,000** — a difference of about 5.3x between the two ends. All of these are calculated from published prices, not quoted rates.

| Workload | Hobby (≈$0.49/1K credits) | Advanced (≈$0.09/1K credits) | Bright Data Web Unlocker |
| --- | --- | --- | --- |
| Standard page (1 credit) | ≈$0.49 / 1,000 | ≈$0.09 / 1,000 | $1.50 / 1,000 |
| Amazon (5 credits) | ≈$2.45 / 1,000 | ≈$0.46 / 1,000 | $1.50 / 1,000 |
| Standard + JS rendering (11 credits) | ≈$5.39 / 1,000 | ≈$1.01 / 1,000 | $1.50 / 1,000 |
| Google (25 credits) | ≈$12.25 / 1,000 | ≈$2.30 / 1,000 | $1.50 / 1,000 (SERP API) |

The Google row is where the cheap-alternative story breaks down. A Google request costs 25 credits, so on Hobby you're paying about $12.25 per 1,000 SERP calls against Bright Data's $1.50 per 1,000 on its SERP API. Unless you're on a high-volume tier, or you're fetching Google result pages as ordinary HTML rather than through the structured endpoint, ScraperAPI is the more expensive option for search results. The same logic applies to any list dominated by LinkedIn or ultra-premium targets.

👉 [Check which plan's credit rate fits your request mix](https://www.scraperapi.com/pricing/?fp_ref=coupons)

Before committing, count your monthly requests by type, multiply by the credit cost above, and compare the total against the plan allowance. ScraperAPI's dashboard has a Domain Cost Estimator that reports the credit cost for any URL, and the `max_cost` parameter caps what a single request can spend. The 5,000 trial credits are enough to measure your real mix on real URLs.

## What ScraperAPI replaces, and what it doesn't

ScraperAPI's own write-up positions it as a replacement for Web Unlocker, the SERP API, the Web Scraper API, the Browser API and Crawl-style jobs. It handles blocking, retries and site layout changes, and returns JSON from structured endpoints for Amazon, Google, ChatGPT, Walmart, eBay and Redfin. DataPipeline runs scheduled projects of up to 100,000 URLs; Async batch jobs accept up to 50,000 URLs with automatic retries for up to 24 hours.

It does **not** sell standalone proxies, raw per-GB bandwidth or mobile proxies. If your Bright Data spend is mostly proxy traffic, ScraperAPI can't take that line item. Its region targeting is also narrower than you might assume: Hobby and Startup cover the US and EU only, and country-level targeting starts at Business.

Bright Data's own list of things it does that a scraping API generally doesn't: city and ZIP-level targeting, Playwright sessions up to 60 minutes, 1,280 pre-built scrapers across 1,188 domains, a dataset marketplace, and ISO 27001/27017/27018 certifications for procurement.

## The split-route model, with the arithmetic

The cheapest configuration for a mixed list usually isn't a migration. It's routing by domain.

Take 250,000 pages a month, 50,000 of them on three protected retail sites. Sending everything through Bright Data Web Unlocker at pay-as-you-go rates costs $375. Split it: the 50,000 protected pages stay on Web Unlocker at $75, and the 200,000 public pages go to a per-page API.

On ScraperAPI, those 200,000 standard pages need 200,000 credits. Hobby covers 100,000 of them for $49, so the first 100,000 pages cost about $0.49 per 1,000 — well under a third of the Web Unlocker rate. Beyond that allowance you'd need a larger tier; the pricing page has the current numbers, and credits don't roll over, so size for your busiest month rather than the average. For many teams the public share alone justifies a ScraperAPI plan, and the protected domains never move.

The same logic applies to turning off custom headers. If a Bright Data target only needs your cookies for one flow, isolate that flow rather than enabling the feature across a zone, and your failed requests stop being billed.

## How the other options compare

A short, purely informational survey of what else shows up in this comparison. These are list prices as published; check them before you buy.

**Oxylabs Web Unblocker** bills by gigabyte rather than request: $30/month at $7.20/GB, $100 at $6.00/GB, $500 at $4.80/GB, enterprise from $2,500 at $3.00/GB. Billing is success-based and JS rendering is included. A 100 KB page works out around $0.72 per 1,000; a 500 KB page around $3.60. Light pages are cheap, heavy pages are not. Oxylabs still sells mobile proxies, which Bright Data's new customers can no longer order.

**ZenRows** uses credits: 1 for a plain page, 5 with rendering, 10 with premium proxies, 25 with both. A protected rendered page runs $2.28 per 1,000 on Scale to $8.89 on Build. Failures aren't billed; 404 and 410 count as successes.

**Zyte API** prices by site difficulty, from $0.13 to $1.27 per 1,000 for HTTP and $1.01 to $16.08 for browser rendering, charged only on successful responses.

**Decodo** (formerly Smartproxy) starts residential at $11.25/month for 3 GB ($3.75/GB), or $4/GB pay-as-you-go, with a scraping API from $19/month for up to 38,000 pages and a free plan capped at 10,000 pages a month. Its advertised pool is 115M+ IPs against Bright Data's 400M+ claim.

**ScrapingBee** is $49/month for 250,000 credits and 50 concurrent requests, with requests costing 5 credits with JS, 10 with premium proxies, 25 with both.

**Firecrawl** charges 1 credit per page, from $16/month billed annually ($19 monthly) for 5,000 credits and 5 concurrent jobs, aimed at LLM-ready markdown output.

**MeshArc** runs $29, $99 and $349 tiers plus enterprise from $1,500, charging by how each page was read: plain pages from $0.14 per 1,000, blocked pages and unchanged pages free.

The pattern across all of them: per-GB pricing rewards small pages and punishes heavy ones; per-credit pricing rewards simple targets and punishes search results and social sites. Bright Data's flat $1.50 is the simplest to forecast and the most expensive for easy pages.

## Who should stay on Bright Data

Keep Bright Data if any of these describe you:

- You need the raw proxy network, including mobile proxies. ScraperAPI has no proxy product at all; Bright Data's new customers can no longer order mobile proxies, and there's been no formal announcement of a withdrawal, but the option is gone from its pricing pages and product navigation.
- You depend on the dataset marketplace or the 1,280 pre-built scrapers. ScraperAPI doesn't sell datasets.
- You need city or ZIP-level geotargeting, or scripted Playwright sessions of up to 60 minutes.
- Procurement requires ISO 27001/27017/27018 certification.
- Every target on your list is a heavily protected page that needs residential rendering every time. At that point the per-page premium of an unlocker is buying something real, and the flat rate is competitive.

Switch considerations flip if your list is mostly public pages, or if a large share of your Bright Data bill is failed requests from custom headers.

## FAQ

**Can ScraperAPI replace Bright Data Web Unlocker entirely?**
For page reading, largely yes: it handles blocking, retries, rendering and structured extraction from one credit balance. It cannot replace the proxy network, mobile proxies or datasets. Teams using several Bright Data products usually end up splitting rather than migrating.

**Are failed requests charged?**
ScraperAPI bills only successful 200 and 404 responses, so failed 500 responses are free. On Bright Data, failures are free by default but get billed once you enable custom headers, cookies or manual element waits.

**How much can I test for free?**
ScraperAPI gives 7 days and 5,000 credits without a card, then a free plan of 1,000 credits a month at 5 concurrent threads. Bright Data gives 5,000 free requests a month, which stops once you move to a committed plan.

**Why does a Google request cost 25 credits?**
Search engines are among the most aggressively protected targets, and ScraperAPI prices the parsing and bypass work accordingly. If SERP data is a large part of your volume, compare per-1,000 costs against Bright Data's SERP API before switching; on Hobby, ScraperAPI is the more expensive of the two for this workload.

**Does Bright Data still offer mobile proxies?**
New customers can't order them. They've been removed from the proxy pricing page and product navigation, and there's no official announcement explaining the change, so treat it as unavailable rather than discontinued.

## How to decide

Match the plan to your request mix, not to the headline credit number:

- **Only public pages, monthly billing** → Hobby at $49/month covers 100,000 credits at 20 threads, and standard pages land near $0.49 per 1,000.
- **Public pages plus a few protected domains** → keep those domains on Bright Data and move the rest to ScraperAPI. The protected share stays at $1.50 per 1,000, the public share drops below a third of that.
- **Google, LinkedIn or ultra-premium heavy** → run the credit math first. The per-page advantage disappears on Hobby, and you need volume before Advanced's $0.09 per 1,000 credits rescues it.
- **Proxy traffic, datasets, city-level targeting** → stay on Bright Data and renegotiate the tier instead.

Two things to confirm before you check out: your real blended cost per 1,000 pages after weighting each request type, and whether your target countries fall inside Hobby's US and EU coverage. Both are answerable in the trial.

👉 [Start the 7-day ScraperAPI trial and price your own request mix](https://www.scraperapi.com/?fp_ref=coupons)
