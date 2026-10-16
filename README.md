# vps hosting pricing: what plans really cost per month, the fees most pages hide, and how to pick the right one

An entry-level VPS runs between $2.50 and roughly $10 a month right now across the major providers. For that money you get one or two vCPUs, between 512MB and 2GB of RAM, and anywhere from half a terabyte of bandwidth to unlimited. A plan that can comfortably run a small production site — 2 to 4GB of RAM — lands in the $5 to $15 range, and dedicated-CPU or memory-optimized servers start around $42 to $84 at DigitalOcean.

Sticker prices are only half the story, though. What you'll actually pay depends on billing terms (intro rates that expire after three months, multi-year commitments, annual-only plans), on add-ons like backups and extra IP addresses, and on how much server admin you're willing to do yourself. This guide walks through current VPS hosting pricing from the providers people actually compare, uses RackNerd as the worked example at the budget end, and adds up the fees that pricing tables tend to leave out.

> **Quick take:** for a blog, a staging server, or a lightweight app, RackNerd's 1GB KVM plan — 1 vCPU, 1GB RAM, 20GB SSD, 2TB bandwidth at $4.98/month — is the sensible middle of its lineup. One thing to know before you click: RackNerd advertises yearly totals rather than monthly rates, so you'll pay for a year up front. 👉 [Check RackNerd's current plans and yearly pricing](https://bit.ly/my-rn)

## What VPS hosting actually costs right now

Most providers cluster between $3 and $5 for their cheapest plan. The entry number matters less than what it buys, because the cheapest plans differ wildly in RAM, storage, and bandwidth.

The figures below come from a price comparison site that says it hand-checked every plan in early February. Hetzner and Contabo quote in euros; the rest use US dollars.

| Provider | Entry price | Data center locations | Advertised uptime |
| --- | --- | --- | --- |
| Vultr | $2.50 | 32 | 99.95% |
| Hetzner | €3.29 | 6 | 99.9% |
| OVHcloud | $3.50 | 30 | 99.9% |
| DigitalOcean | $4.00 | 15 | 99.99% |
| Hostinger | $4.99 | 7 | 99.9% |
| Contabo | €4.99 | 8 | 99.9% |
| Linode (Akamai) | $5.00 | 11 | 99.9% |
| RackNerd | $10.28* | 10 | 99.9% |

*RackNerd quotes yearly totals rather than monthly rates, so its entry price reads differently depending on the listing. Its KVM plans work out lower on a monthly-equivalent basis, as the next section shows.

A few entry tiers are worth calling out by config. Vultr's $2.50 plan is genuinely minimal: 1 vCPU, 512MB RAM, 10GB SSD, 0.5TB bandwidth. OVHcloud's $3.50 Starter includes 2GB of RAM — the most of any entry tier in this group — but quotes bandwidth as a 100Mbps port instead of a monthly quota. Contabo's €4.99 is the standout on raw specs at 4 vCPUs, 8GB RAM, 50GB NVMe, and unlimited traffic, if you can live with eight data center locations to choose from.

The pattern to internalize: between $2.50 and $5, you're shopping for either the lowest possible bill (Vultr, RackNerd) or the most hardware per dollar (Contabo, Hetzner). Past $5, configs open up fast — Hostinger's KVM 1 at $5.99 already includes 4GB of RAM on NVMe storage with 4TB of bandwidth.

## RackNerd's plans and pricing

RackNerd sits at the budget end of the market: a 4.4/5 rating in the comparison, ten data center locations, and 99.9% advertised uptime. Its lineup is built around KVM plans billed as annual totals. Three plans have published, comparable configs:

| Plan | vCPU / RAM | SSD storage | Bandwidth | Price (monthly equiv.) | Buy |
| --- | --- | --- | --- | --- | --- |
| 512MB KVM | 1 / 512MB | 10GB | 1TB | $1.92 | [Get 512MB KVM](https://bit.ly/my-rn) |
| 1GB KVM | 1 / 1GB | 20GB | 2TB | $4.98 | [Get 1GB KVM](https://bit.ly/my-rn) |
| 2GB KVM | 2 / 2GB | 40GB | 3TB | $9.48 | [Get 2GB KVM](https://bit.ly/my-rn) |

Multiply those monthly equivalents out and you're paying roughly $23, $60, or $114 for the year, up front. That's the trade: a lower effective rate in exchange for prepaying and less month-to-month flexibility. If the plan turns out to be wrong for your workload, your money is already spent.

Honest assessment time. The 512MB KVM at $1.92 is the lowest named price anywhere in this comparison, and the 2GB plan at $9.48 undercuts DigitalOcean's closest regular plan ($12 for 2 vCPU, 2GB, 2TB) on both price and bandwidth. At the same time, Hostinger's KVM 2 at $10.99 doubles the RAM to 8GB, and Hetzner's CPX11 at €5.49 matches 2 vCPU and 2GB for nearly half the price with 22TB of bandwidth. RackNerd's edge is the bottom of the price range and the pay-once-a-year model — specs per dollar at the $5–11 tier belong to Contabo and Hetzner.

## Billing terms change the real price

The monthly figure on the plan card is often a starting rate, and the fine print determines your year-one total.

IONOS is the clearest example because it shows both numbers. Its VPS S+ lists at $6/month, with $2/month for the first three months on a one-year term. Do the math: $6 for the intro stretch, $54 for the remaining nine months, $60 in year one — an effective $5/month, then $72/year at renewal. The "$2/month" headline is technically true and practically misleading if you take it at face value. The same structure applies up the range: VPS XL+ goes from $14 intro to $47 regular.

GoDaddy plays a longer game. Its $8.99 entry plan (1 vCPU, 2GB RAM, 40GB NVMe) is priced for the first three-year term — about $324 committed over three years — and the renewal rate isn't something you'll see on the plan card itself. Confirm it in the cart before signing up for three years, because that's a long time to be surprised.

RackNerd, as covered above, folds its discount into annual totals instead. DigitalOcean is the opposite: its $4 Basic plan is plain month-to-month with no term condition, which makes it the easiest to reason about and the easiest to walk away from. vps.org takes flexibility further with hourly billing capped at the monthly rate — its Starter plan is $0.005/hour — plus a 30-day money-back guarantee, which suits short-lived test projects.

> One rule covers most of this: before any plan with a term attached — one year or three — find the renewal figure first. Intro pricing only tells you what year one costs.

## The fees VPS pricing pages leave out

Base price rarely equals total price. A handful of add-ons show up either at checkout or the first time you actually need them:

| Add-on | What it usually costs | Verified examples |
| --- | --- | --- |
| Automated backups | 20–30% of the plan's monthly price | vps.org: 30% for daily backups (7-day retention), 20% for weekly (28-day); IONOS Cloud Backup from $0.065/GB per month |
| Extra IPv4 address | $1–5 per month | vps.org $1/month; IONOS $5/month (one IPv4 included per server) |
| Control panel | Often billed separately | IONOS lists Plesk Obsidian at $6/month; GoDaddy offers cPanel or Plesk as options across its plans |
| Bandwidth overage | A few dollars per TB beyond your quota | Standard practice; Contabo and vps.org instead list unlimited traffic under fair use |
| Domain name | $9–15 per year | vps.org $9–12/year; IONOS from $1/year |

Two things you generally shouldn't pay for: a TLS certificate (Let's Encrypt is free) and, on budget plans, fancy extras you haven't hit a wall without yet.

The biggest invisible cost is your own time. Patching, monitoring, and the occasional 2 a.m. recovery are what managed hosting actually sells — GoDaddy runs a fully managed tier, and DigitalOcean points self-managers who want out toward Cloudways. If you'd rather never touch a package manager, that premium may be worth it; if you enjoy the work, skip it.

## Which plan fits your situation

Match the plan to the workload, in rough order of how common the workload is:

- **Learning, testing, throwaway projects.** Take the cheapest tier and don't overthink it — RackNerd's 512MB KVM at $1.92 or Vultr's $2.50. Just know 512MB fits a bare Linux box and one small service, and not much more.
- **A small production site or app with a database.** Aim for 2–4GB of RAM. RackNerd's 2GB KVM ($9.48, 2 vCPU, 3TB) works; Hostinger's KVM 1 ($5.99, 4GB) and Hetzner's CX23 (€5.49, 2 vCPU, 4GB, 22TB) buy more headroom for similar money. If you'd rather stay annual and low-commitment, 👉 [compare RackNerd's 1GB and 2GB KVM plans](https://bit.ly/my-rn) before deciding how much RAM you really need.
- **Databases, caches, in-memory workloads.** DigitalOcean's Memory-Optimized line starts at $84/month for 16GB RAM and 2 vCPUs. Contabo's VPS M (€8.99, 6 vCPU, 16GB, unlimited traffic) is the budget alternative if location flexibility matters less.
- **CPU-bound work — CI/CD, video encoding, batch jobs.** DigitalOcean's CPU-Optimized plans start at $42/month with a 2:1 RAM-to-CPU ratio; Contabo's VPS L (€14.99, 8 vCPU, 30GB) is the raw-power play.
- **Large datasets.** DigitalOcean's Storage-Optimized servers start at $131/month with 300GB NVMe and scale to 7TB.
- **Windows Server required.** GoDaddy supports Windows from its $17.99 tier up (the $8.99 entry plan is Linux-only); IONOS lists Windows Server 2022 and 2025 across its VPS+ range.
- **You want someone else on call.** GoDaddy's managed plans or Cloudways on top of DigitalOcean — paying more to never SSH in is a legitimate choice.

## VPS pricing FAQ

**Do cheap VPS prices go up when you renew?**
Depends entirely on the provider. IONOS is explicit about it ($2 becomes $6 after three months), GoDaddy ties its rate to a first three-year term, RackNerd folds its pricing into annual totals, and DigitalOcean lists straightforward monthly rates with no term language. Whenever a term is involved, get the renewal number before paying.

**Is monthly, annual, or hourly billing smarter?**
Annual wins on price if you'll use the server all year and trust the provider — that's the whole RackNerd model. Hourly billing (vps.org, capped at the monthly rate) makes sense for short projects you'll tear down in weeks. Plain monthly (DigitalOcean) is the right call when you might resize or cancel on short notice.

**Is a $2–4 VPS actually usable?**
For lightweight sites, proxies, bots, and test environments, yes — people run real things on 512MB–1GB boxes every day. For a busy database, a Java application, or anything with traffic spikes, no; you'll want 2GB minimum and ideally 4GB, which puts you in the $5–15 band.

## Before you pay

Three quick scenarios to orient you. Want the lowest possible yearly bill and don't mind prepaying? That's RackNerd's territory, and the 512MB and 1GB KVM plans are its strongest value. Need to keep every option open month to month? DigitalOcean at $4 or vps.org's hourly billing. Chasing maximum specs per dollar or euro? Contabo, no contest. Need Windows or managed support? GoDaddy or IONOS.

Before checkout, confirm three things: your bandwidth quota covers your actual traffic (overage runs a few dollars per TB), you've added automated backups if the data matters (budget 20–30% on top), and you know the renewal rate if a term is involved. If the annual-prepay model fits how you work, 👉 [lock in RackNerd's yearly pricing before you deploy](https://bit.ly/my-rn) — it's the cheapest way into this whole comparison.
