# bandwagonhost stock checker: how to read the live stock page, catch CN2 GIA restocks, and order a plan that's in stock

Landing on "out of stock" at BandwagonHost means something very specific: the node that hosts that exact configuration in that datacenter is full, and the company won't oversell it. Because BandwagonHost provisions everything on its own hardware, a plan can sit red for weeks and flip green without warning — usually right after new capacity comes online or existing customers cancel. A BandwagonHost stock checker turns that from a guessing game into a routine: one live page shows every sellable plan as green or red, and a few third-party monitors add alerts and history on top.

This guide covers where to check stock, what the trackers showed as of mid-September 2026, the full plan list with verified prices, restock timing patterns, and what to do when the exact plan you want is red.

> **Short version:** if you want China-optimized CN2 GIA-E routing without waiting on a restock, the E-Commerce 20G plan at **$49.99/quarter** (or $169.99/year) has stayed reliably in stock, and you can migrate between CN2 GIA-E datacenters for free afterward. Tight budget and no China-route requirement? The 20G KVM at $49.99/year is the cheap, nearly-always-green option. 👉 [Open BandwagonHost's plan catalog and live stock status](https://bwh81.net/aff.php?aff=77528&gid=1)

## Why BandwagonHost plans go out of stock

Two mechanisms cause it: node capacity limits for regular plans, and small batch releases for limited editions. They call for different responses.

Regular plans fill up node by node. BandwagonHost is operated by IT7 Networks, a Canadian company that has run the service since 2004, and it provisions only on its own enterprise hardware — RAID-10 SSD arrays, with NVMe on the newer Hong Kong, DC9, and Vancouver nodes. The real bottleneck is China-optimized bandwidth. BandwagonHost's own CN2 GIA page notes that ordinary transit to China can hit 30% packet loss during peak hours, and that CN2 GIA transit pricing reached roughly $120 per megabit at one point. The company operates eight 10 Gbps CN2 GIA/CTGNet links in Los Angeles across two datacenters, plus CN2 GIA in Hong Kong and Japan, and each datacenter gets a fixed pool of that premium capacity. When the slots for, say, the 1GB CN2 GIA-E tier in DC6 or DC9 fill up, the tier goes red until new hardware arrives or someone cancels. Recent hardware additions in Hong Kong, Los Angeles DC9, and Vancouver have reopened slots, but the cheapest tiers in the most popular DCs still gap out regularly.

Limited editions work differently. Plans like THE PLAN, MINICHICKEN, the Box family, and The Tokyo Plan are released in small batches with no published schedule. A batch sells out — the $19/year MINICHICKEN once went in a single morning — then goes quiet until the next drop, which could be weeks away or the next day.

## The stock checkers you can use

Three layers, from official to community, and each catches things the others miss.

### BandwagonHost's own stock page

Start here. BandwagonHost runs a real-time inventory page (stock.bwg.net) that refreshes roughly every five minutes and lists every sellable plan as green or red, grouped by plan family — CN2 GIA-E, Hong Kong, Osaka, and the limited editions each get their own rows. Green means the order button will work. Red means it won't, no matter how many times you refresh the checkout.

### Third-party monitors with alerts

HostMonit and several community-run tracker sites poll the order pages continuously and add two things the official page doesn't: restock alerts pushed to Telegram or QQ groups, and stock history, so you can tell whether a plan has been red for two days or two months. One tracker's snapshot on September 14, 2026 counted 55 plans in stock and 20 out, with every regular KVM PROMO and E-Commerce tier green. Limited editions are the flip side — BiggerBox Pro and MegaBox Pro were both marked out of stock in recent snapshots.

### Community restock alerts

BWH-focused threads on LowEndTalk, NodeSeek, and V2EX tend to post restock alerts within minutes of a drop. If you're chasing one specific limited edition, this is usually how people hear about it first.

## A checking routine that catches restocks

The routine that works is boring and specific:

1. Park the stock page in a browser tab and leave it open.
2. Filter down to the plan family you're chasing, so you only scan one row.
3. If your plan is red and you're flexible, look for what's green in the same tier — a different datacenter or the next configuration up.
4. If it's a limited edition, check once in the morning and once in the evening. Restocks have shown up at random hours.
5. When a row flips green, open the order link and check out in the same session.

That last step decides outcomes. One catalog guide describes watching the CN2 GIA-E 10G limited edition go green, deliberating for ten minutes, and coming back to find it gone. Limited slots have disappeared in under an hour, and the cheapest batches have sold out in a single morning.

## The full plan list: prices, cycles, and stock status

Everything below reflects the current catalog, with stock status from the September 14, 2026 tracker snapshot. Stock changes daily, so treat that column as a reference point rather than a promise — confirm on the live page before ordering.

### KVM PROMO plans (general-purpose, multi-datacenter)

| Plan | CPU / RAM / SSD | Traffic | Price | Stock (Sep 14) | Order |
| --- | --- | --- | --- | --- | --- |
| 20G KVM PROMO | 2C / 1 GB / 20 GB SSD | 1 TB | $49.99 / yr | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=44) |
| 40G KVM PROMO | 3C / 2 GB / 40 GB SSD | 2 TB | $52.99 / 6 mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=45) |
| 80G KVM PROMO | 4C / 4 GB / 80 GB SSD | 3 TB | $19.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=46) |
| 160G KVM PROMO | 5C / 8 GB / 160 GB SSD | 4 TB | $39.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=47) |
| 320G KVM PROMO | 6C / 16 GB / 320 GB SSD | 5 TB | $79.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=48) |
| 480G KVM PROMO | 7C / 24 GB / 480 GB SSD | 6 TB | $119.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=49) |

The 20G tier alone can be hosted in eight datacenters (DC2, DC4, DC8, FMT, USNJ, USNY, CABC_1, and EUNL_3), and the 40G tier also has an annual option at $99.99/year. None of these lines are China-optimized — they're the workhorses for general hosting, learning boxes, and low-traffic sites.

### CN2 GIA-E E-Commerce and SLA plans

| Plan | CPU / RAM / SSD | Traffic | Price | Stock (Sep 14) | Order |
| --- | --- | --- | --- | --- | --- |
| 20G CN2 GIA-E (E-Commerce) | 2C / 1 GB / 20 GB SSD | 1 TB | $49.99 / qtr | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=87) |
| 40G CN2 GIA-E (E-Commerce) | 3C / 2 GB / 40 GB SSD | 2 TB | $89.99 / qtr | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=88) |
| 80G CN2 GIA-E (E-Commerce) | 4C / 4 GB / 80 GB SSD | 3 TB | $56.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=89) |
| 160G CN2 GIA-E (E-Commerce) | 6C / 8 GB / 160 GB SSD | 5 TB | $86.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=90) |
| 20G E-Commerce SLA (LA) | 2C / 1 GB / 20 GB NVMe | 1 TB | $65.89 / qtr | In stock | [ Order](https://bwh81.net/aff.php?aff=77528) |
| 40G E-Commerce SLA (LA) | 3C / 2 GB / 40 GB NVMe | 2 TB | $116.99 / qtr | In stock | [ Order](https://bwh81.net/aff.php?aff=77528) |
| 80G E-Commerce SLA (LA) | 4C / 4 GB / 80 GB NVMe | 3 TB | $69.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528) |

E-Commerce plans are multi-datacenter — DC6 CN2 GIA-E, DC9 CN2 GIA, JPOS_1 Softbank Osaka, and EUNL_9 China Unicom Premium Amsterdam, among others. The SLA variants are Los Angeles only, run NVMe storage, and combine CN2 GIA with China Unicom Premium (AS10099) and CMIN2 routes. The E-Commerce 20G tier is also offered at $169.99/year instead of quarterly billing.

### Regional CN2 GIA plans (fixed datacenter)

| Plan | CPU / RAM / SSD | Traffic | Price | Stock (Sep 14) | Order |
| --- | --- | --- | --- | --- | --- |
| Dubai 20G | 2C / 1 GB / 20 GB SSD | 500 GB | $19.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=114) |
| Dubai 40G | 3C / 2 GB / 40 GB SSD | 1 TB | $32.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=115) |
| Dubai 80G | 4C / 4 GB / 80 GB SSD | 2 TB | $56.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=116) |
| Dubai 160G | 6C / 8 GB / 160 GB SSD | 3 TB | $86.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=117) |
| Osaka 40G | 2C / 2 GB / 40 GB SSD | 500 GB | $49.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=134) |
| Osaka 80G | 4C / 4 GB / 80 GB SSD | 1 TB | $86.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=135) |
| Singapore 40G | 2C / 2 GB / 40 GB SSD | 500 GB | $49.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=173) |
| Singapore 80G | 4C / 4 GB / 80 GB SSD | 1 TB | $86.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=174) |
| Tokyo 40G CN2 GIA | 2C / 2 GB / 40 GB SSD | 500 GB | $89.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528) |
| Hong Kong 40G CN2 GIA | 2C / 2 GB / 40 GB SSD | 500 GB | $89.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528) |
| Hong Kong 80G CN2 GIA | 4C / 4 GB / 80 GB SSD | 1 TB | $155.99 / mo | In stock | [ Order](https://bwh81.net/aff.php?aff=77528&pid=96) |

Port speeds, where published: 1 Gbps on the KVM PROMO line, 1.5 Gbps on the Osaka and Singapore CN2 GIA tiers, 2.5 Gbps on the E-Commerce and SLA lines.

### Limited editions (batch releases)

| Plan | Config | Price | Stock (Sep 14) | Order |
| --- | --- | --- | --- | --- |
| THE PLAN | 2C / 2 GB / 40 GB, 1 TB traffic, 17+ premium DCs incl. DC6 CN2 GIA-E and DC9 | $99 / yr | Batch release | [ Order](https://bwh81.net/aff.php?aff=77528) |
| BiggerBox Pro | 1C / 1 GB / 20 GB, 1 TB at 2.5 Gbps, CN2 GIA + CMI + CUP tri-network | $39 / yr | Out of stock | [ Order](https://bwh81.net/aff.php?aff=77528) |
| MegaBox Pro | 2C / 2 GB / 40 GB, 2 TB at 2.5 Gbps, Los Angeles | $49 / yr | Out of stock | [ Order](https://bwh81.net/aff.php?aff=77528) |
| MINICHICKEN | Capped at 25% of one core, small-batch budget plan | $19 / yr | Batch release | [ Order](https://bwh81.net/aff.php?aff=77528) |

"Batch release" means the row only shows stock immediately after a drop. Other batch plans rotate through the catalog too — THE PLAN v2, THE CHICKEN, MiniBox, BiggerBox, PowerBox, SakuraBox, FREEDOM PLAN, The DC9 Plan, The Tokyo Plan, The DC6 Plan ($53/year), and The Amsterdam Plan ($39/year). Check the CPU caps before chasing any of them: MINICHICKEN and BiggerBox are capped at 25% of one core, THE PLAN at 45% — fine for proxies and small sites, frustrating for anything CPU-heavy.

Billing cycles change the real cost more than most people expect. The E-Commerce 20G plan runs $199.96 over a year of quarterly billing versus $169.99 on the annual cycle — same plan, about $30 apart. The 40G KVM PROMO is $105.98 a year on the semi-annual cycle versus $99.99 annual. And the $49.99/year limited-edition CN2 GIA-E works out to roughly a quarter of what the equivalent regular plan costs over a year of quarterly billing. That's the trade-off in one number: much lower price, availability nobody can schedule.

## Out of stock on the plan you wanted? Three moves

Buy a green datacenter and migrate, step the configuration up or down, or wait for a drop — roughly in that order of practicality.

**Buy the same tier in a green datacenter, then migrate.** Most CN2 GIA-E and E-Commerce plans ship with free migration across the DC pool, so if DC9 is full, DC6 or SJC5 might not be. You order wherever the row is green, then move to your preferred datacenter in KiwiVM once you're in. Migration keeps your traffic allowance and costs nothing.

**Step the configuration up or down.** The 1GB CN2 GIA-E tier gaps out most often; the 2GB tier at $89.99/quarter is almost always available by comparison, and most 1GB workloads fit comfortably in 2GB. 👉 [See current stock for the 40G CN2 GIA-E plan](https://bwh81.net/aff.php?aff=77528&pid=88) — Going the other direction, the 20G KVM at $49.99/year skips CN2 routing entirely but stays green for general-purpose use.

**Wait for a limited-edition drop — only if you can afford to.** The savings over the regular equivalent are genuine, and the $49.99/year and $89.99/year CN2 GIA-E limited editions do come back. But there's no schedule, so if you have a deadline, don't bet on a drop landing in time.

## Restock timing: patterns worth knowing

There is no fixed restock schedule. Drops happen when BandwagonHost secures additional CN2 GIA bandwidth allocation, and a tracker that has logged inventory for 12 months reports gaps of roughly two to six weeks between restocks. The best odds sit on weekday mornings between 9 a.m. and 12 p.m. US Pacific, when most restocks have landed. Speed matters once a drop goes live: the cheapest tiers have historically sold out in two to four hours, and the next tier up in six to twelve.

Event windows concentrate the drops — Double 11 (November 11), Black Friday, and Chinese New Year. Through 2025, several limited plans (MINICHICKEN, BiggerBox Pro, The Tokyo Plan v2, and The Amsterdam Plan) restocked between May and July. None of this guarantees anything; it just tells you when to look.

## Set yourself up to check out fast

Four things done in advance beat any amount of refreshing. Create your account and save a payment method now, so checkout takes under a minute when stock appears. Bookmark the order page for the plan you want so you skip the browsing. Pick annual billing where it exists — the cycle math above shows where it saves money, and it locks the price. Then, when the row flips green, treat it as a starting gun: same-session checkout, no tab-hoarding. 👉 [Open the 20G CN2 GIA-E order page — $49.99/quarter or $169.99/year](https://bwh81.net/aff.php?aff=77528&pid=87)

## BandwagonHost stock checker FAQ

**Does "out of stock" mean the plan is discontinued?** No. Out of stock means that specific configuration in that specific datacenter has no free provisioning capacity right now. Plans come back when hardware is added or slots free up, and limited editions come back as new batches.

**How fast do restocks sell out?** The cheapest tiers have gone in two to four hours historically, and limited editions sometimes in under an hour. Higher-priced tiers last longer because fewer people buy them.

**When should I check?** Weekday mornings between 9 a.m. and 12 p.m. US Pacific for regular restocks, twice daily for limited editions, and expect concentrated drops around Double 11, Black Friday, and Chinese New Year.

**Where do restock alerts come from?** Community threads on LowEndTalk, NodeSeek, and V2EX, plus the Telegram and QQ notification groups run by the monitor sites.

## Which plan to pick, based on your deadline

- **Need a China-optimized VPS this week:** the E-Commerce 20G at $49.99/quarter (or $169.99/year) — in stock, and free migration lets you land on the best DC after the fact.
- **Tightest possible budget:** the 20G KVM at $49.99/year; if you need more resources, the 80G KVM at $19.99/month is the odd bargain of the catalog.
- **Chasing a limited edition:** account created, payment saved, stock page checked morning and evening, checkout the moment the row goes green.
- **Can't wait at all:** RackNerd sells budget plans with occasional CN2 (not GIA-grade) routing and flash sales from around $10.88/year, and DMIT is a premium CN2 GIA provider in Los Angeles and Tokyo starting at $39.99/quarter that is usually in stock. Both trade either route quality or money for availability.

Whatever you pick, the sequence is the same: confirm the row is green, then check out immediately. 👉 [Browse BandwagonHost's full plan list and see what's green right now](https://bwh81.net/aff.php?aff=77528&gid=1)
