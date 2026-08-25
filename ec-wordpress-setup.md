# EXPLORE CLAIREMONT — WordPress Dashboard Documentation

**Site:** EXPLORE CLAIREMONT
**Tagline:** "Serving The Heart Of San Diego"
**URL:** https://exploreclairemont.com
**Documented on:** August 25, 2026
**Previously documented on:** March 22, 2026 — this file said "March 22, 2026" until this refresh, so anything you remember from the old version is five months stale.

Every figure below was checked live in wp-admin on **August 25, 2026** unless the line says otherwise. A handful of numbers could not be re-read without changing something on the site; those are marked **(last checked March 2026)** and should be treated as unverified.

---

## 1. SITE OVERVIEW (At a Glance)

| Metric | Count (Aug 25, 2026) | Was (Mar 22, 2026) |
|---|---|---|
| Posts | 61 published (62 total, 1 draft) | 40 published (41 total) |
| Pages | 87 published (97 total: 9 drafts, 1 private) | 77 published (86 total) |
| Comments | 200 (all approved; 0 pending, 0 spam, 0 trash) | 90 |
| Listings | 1,518 total (1,513 published, 5 drafts) | 1,456 published |
| Events | 1,394 total (1,353 published, 41 drafts) | 692 |
| Special Offers | 8 total (7 published, 1 draft) | not tracked |
| Newsletters | 48 published | not tracked |
| Contest Entries | 31 total (28 published, 3 drafts) | not tracked |
| Punch Cards | 1 (draft) | not tracked |
| Local Scroll Photos | 21 approved, 0 pending | not tracked |
| Site Reviews | 18 (all approved) | 15 |
| Users | 2,783 | 1,632 |
| Media Files | 1,425 (1,243 uncategorized) | 1,150 |
| WordPress Version | **7.1** (up to date) | 6.9.4 |
| Active Theme | **Bricks Child Theme** 1.1 | same |

The two headline movers are **Events, which roughly doubled** (692 to 1,394 — the event aggregator pipeline is working), and **Users, up about 70%** (1,632 to 2,783).

---

## 2. GENERAL SETTINGS

- **Site Language:** English (United States / en_US)
- **Timezone:** America/Los_Angeles (UTC-7, currently in DST)
- **Permalink structure:** `/%postname%/`
- **Membership:** Anyone can register — yes
- **Default New User Role:** Contributor
- **Environment:** Production
- **HTTPS:** Enabled
- **Multisite:** No
- **Search engine visibility:** **Indexing is now allowed.** This changed since March, when "Discourage search engines" was switched on. Site Health confirms "Is this site discouraging search engines? No."

**Reading Settings:**
- Homepage: Static page → "Explore Clairemont"
- Posts page: "Blog"
- Posts per page: 10

**Discussion Settings** (unchanged since March):
- Users must be registered and logged in to comment — yes
- Require name and email — yes
- Comment moderation queue — off (comments auto-approve)
- Hold comments if author has no prior approved comment — yes
- Comments open by default on new posts — yes

---

## 3. SERVER / TECHNICAL ENVIRONMENT

| Setting | Value (Aug 25, 2026) | Was (Mar 22, 2026) |
|---|---|---|
| OS / Architecture | Linux 5.14.0-687.39.1.el9_8 x86_64 | Linux 5.14.0-503 x86_64 |
| Web Server | Apache (LiteSpeed SAPI) | same |
| PHP Version | 8.3.33 (64-bit) | 8.3.22 |
| PHP Memory Limit | 1024M | same |
| PHP time limit / max input time | 180s / 600s | not recorded |
| PHP max input variables | 1,000,000 | not recorded |
| WP Memory Limit | 512M | same |
| WP Max Memory Limit | 768M | same |
| Database | MariaDB 10.11.19 | 10.11.13 |
| Max DB Connections | 500 | same |
| Max Allowed Packet | 256 MB | same |
| Table prefix | `to25Z_` | not recorded |
| Upload Max File Size | 100 MB | same |
| Max File Uploads | 20 per request | same |
| Image Editor | WP_Image_Editor_Imagick (ImageMagick 7.1.2-29, Imagick 3.8.1) | ImageMagick 7.1.1-47 |
| Object Cache | Redis (drop-in active) | same |
| Opcode cache | Enabled, **full** — 128 MB of 128 MB used, interned strings 100% of 8 MB, hit rate 93.31% | not recorded |
| WP_DEBUG | **Disabled** | true |
| WP_DEBUG_LOG | **Disabled** | file-based logging on |
| WP_CACHE | Enabled | not recorded |
| EMPTY_TRASH_DAYS | 30 | not recorded |
| cURL Version | 8.21.0 / OpenSSL 3.5.5 | 8.14.1 / OpenSSL 3.2.2 |
| WordPress Root | `/home/vpbyzrt/public_html` | same |
| Fonts directory | Does not exist | not recorded |

**Disk Usage:**

| Path | Size (Aug 25, 2026) | Was (Mar 22, 2026) |
|---|---|---|
| WordPress total | 2.55 GB | 2.47 GB |
| Uploads folder | 864.82 MB | 597.31 MB |
| Themes | 77.49 MB | 75.45 MB |
| Plugins | 325.08 MB | 316.74 MB |
| Database | **1.71 GB** | 858.08 MB |
| **Grand Total** | **5.49 GB** | ~4.27 GB |

The database doubled in five months. That tracks with events, users and email logs all growing, but it is the number to watch.

---

## 4. THEMES

| Theme | Version | Status |
|---|---|---|
| **Bricks Child Theme** (bricks-child) | 1.1 | Active |
| Bricks (bricks) | 2.3.11 | Parent theme — up to date |
| Twenty Twenty | 3.2 | Inactive |

The site is built entirely with the **Bricks visual page builder**. The March "Bricks parent theme out of date" warning is resolved — it was on 2.2 then, it is on 2.3.11 now. Theme auto-updates are disabled.

---

## 5. PLUGINS (44 total, all 44 active)

Nothing is inactive any more. The three inactive plugins listed in March (two Advanced Ads add-ons and Debug Log Manager) are gone or activated. **Auto-updates are disabled on all 44.**

### Active Plugins (44)

| Plugin | Version (Aug 25, 2026) | Was (Mar 22, 2026) | Notes |
|---|---|---|---|
| Admin and Site Enhancements (ASE) Pro | 9.0.2 | 8.5.1 | wpase.com — also drives the grouped admin menu |
| Advanced Themer for Bricks | 3.3.15 | 3.3.14 | Bricks builder add-on |
| Bit Flows | 1.28.2 | 1.17.1 | Automation flows |
| Bit Flows Pro | 1.28.2 | 1.17.1 | |
| Bit Form | 3.2.2 | 2.21.12 | Form builder — major version jump |
| Bit Form Pro | 3.3.0 | 2.13.9 | major version jump |
| Bricksable | 1.6.84 | 1.6.83 | Bricks elements |
| Classic Monks | 2.2.2 | 1.1.7 | Short links, media folders, logs — major version jump |
| Debug Log Manager | 2.5.2 | 2.4.3 (inactive) | **now active**, sits under Tools |
| EC Ads | 1.13.1 | — | **New.** In-house ad manager, replaces Advanced Ads |
| EC Bracket | 1.3.0 | — | **New.** In-house bracket/tournament voting |
| EC Contest | 1.7.5 | 1.7.5 | In-house contest plugin |
| EC Coupons Lite | 1.6.0 | 1.4.3 | In-house coupon/voucher system |
| EC Events Ticketing | 1.1.0 | (custom) | In-house events ticketing |
| EC Merchant Analytics | 2.0.9 | (custom) | In-house merchant analytics |
| Events Calendar | 1.3.1 | (installed) | In-house events management |
| Explore Clairemont Punch Cards | 1.0.0-rc83 | (custom) | In-house loyalty punch cards — still on a release candidate |
| Fast Times Poll Manager | 1.8.2 | (custom) | In-house newsletter polls |
| Fluent Messaging | 2.7.5 | (installed) | |
| Fluent Snippets | 10.56 | 10.53 | Code snippets |
| FluentCommunity | 2.8.1 | (installed) | Community platform |
| FluentCommunity Pro | 2.8.1 | (installed) | |
| FluentCRM | 3.1.13 | (installed) | CRM and email marketing |
| FluentCRM Pro | 3.1.13 | (installed) | |
| FluentSMTP | 2.3.1 | (installed) | Email delivery |
| General Reviews | 1.2.0 | 1.2.0 | In-house reviews |
| MB Favorite Posts | 2.0.10 | 2.0.9 | MetaBox.io |
| Meta Box | 5.14.1 | 5.11.2 | Custom fields |
| Meta Box AIO | 3.10.0 | 3.5.0 | MetaBox all-in-one |
| Next Bricks | 2.3.5 | 2.2.8 | Bricks add-on |
| Perfmatters | 2.6.7 | 2.5.9 | Performance optimization |
| Redis Object Cache | 2.8.0 | 2.7.0 | Redis caching |
| Relevanssi | 4.28.2 | 4.26.1 | Better search — now a top-level admin menu |
| RentCast Shortcodes (Simple) | 1.2.0 | 1.2.0 | Real-estate shortcodes; new to the active list since March |
| Site Reviews | 8.2.2 | 7.2.13 | Was flagged for update in March — done |
| Slim SEO | 4.10.0 | 4.9.1 | SEO |
| Slim SEO Pro | 1.11.0 | 1.9.4 | |
| The Local Scroll | 1.22 | 1.20 | **New to the active list.** In-house photo wall |
| WP Grid Builder | 2.3.5 | 2.3.2 | Grid/filter layout |
| WP Grid Builder – Bricks | 1.3.5 | 1.3.5 | |
| WP Grid Builder – Caching | 1.2.1 | 1.2.1 | |
| WP Grid Builder – Map Facet | 2.0.4 | 2.0.4 | |
| WP Grid Builder – Meta Box | 1.2.0 | 1.2.0 | |
| wpDiscuz | 7.6.64 | 7.6.47 | Was flagged for update in March — done |

### Removed since March
- **Advanced Ads** (2.0.17), **Advanced Ads Pro** (3.0.9), **Advanced Ads – Tracking** (3.0.10) — all uninstalled
- **Advanced Ads – PopUp and Layer Ads** (2.0.3), **Advanced Ads – Sticky Ads** (2.0.4) — were inactive, now gone

### Must-Use Plugins (2)

| Plugin | Version | Was |
|---|---|---|
| CDN Cache Plugin (by Rocket.net) | 1.1.12 | 1.1.4 |
| ClassicMonks Assets Manager | 1.0.7 | 1.0.3 |

### Drop-ins (2)
- `maintenance.php` — custom maintenance message
- `object-cache.php` — Redis Object Cache drop-in

### Updates Available
**None.** WordPress core, all plugins and all themes report up to date as of the last check on August 25, 2026 at 10:14 am PDT. All three March update warnings (Site Reviews, wpDiscuz, Bricks theme) have been cleared.

---

## 5a. CUSTOM PLUGINS BUILT IN-HOUSE

Eleven of the 44 active plugins were written by Tanja for this site. They are not on wordpress.org, there is no vendor to check for updates, and if one of them breaks the fix is in her own code. Knowing which is which matters when diagnosing anything.

| Plugin | Version | What it does |
|---|---|---|
| EC Ads | 1.13.1 | Ad serving, placements, ad groups, advertiser analytics and client reports |
| EC Bracket | 1.3.0 | Bracket-style tournament voting (admin menu: Bracket Manager) |
| EC Contest | 1.7.5 | Contest entries, categories, voting, integrity checks, leaderboards |
| EC Coupons Lite | 1.6.0 | Special offers, voucher issuing and redemption, merchant payout tracking |
| EC Events Ticketing | 1.1.0 | Ticketing and attendee management attached to the Events post type |
| EC Merchant Analytics | 2.0.9 | Per-business traffic and engagement dashboards |
| Events Calendar | 1.3.1 | Event ingestion and display, plus the aggregator cron |
| Explore Clairemont Punch Cards | 1.0.0-rc83 | Loyalty punch cards, check-ins, UGC, raffles, flash deals |
| Fast Times Poll Manager | 1.8.2 | Newsletter polls, including the House of the Week guessing format |
| General Reviews | 1.2.0 | General-purpose review capture |
| The Local Scroll | 1.22 | Reader-submitted photo wall with QR submission flow |

**RentCast Shortcodes (Simple)** 1.2.0 is also a local helper rather than a marketplace plugin — it wraps RentCast real-estate data in shortcodes and has a help page under Tools.

Punch Cards is still on a release candidate build (`1.0.0-rc83`) despite being live in the admin menu with ten sub-pages, which suggests it is the least finished of the eleven.

---

## 6. SITE HEALTH STATUS

Overall status: **Should be improved**. 26 tests passed.

**1 Critical Issue:**
1. **Page cache is detected but the server response time is still slow** (Performance) — caching is working, the server is still slow to respond.

**1 Recommended Improvement:**
1. **A scheduled event is late** (Performance) — a WP-Cron event has not run on time. This is the same warning that was present in March.

**Resolved since March:**
- "Themes waiting to be updated" — Bricks parent theme is now current
- "Site is set to log errors to a potentially public file" — WP_DEBUG and WP_DEBUG_LOG are both disabled now
- "Remove inactive plugins" — there are no inactive plugins left

---

## 7. CONTENT

### Posts (62 total)
- **61 published**, 1 draft
- Author: primarily Tanja Kropf (47 of 62 are hers)
- Recent posts:
  - "Linda Vista's American Legion Post 731 Seeks Help for Restoration" (Aug 19, 2026)
  - "Clairemont Town Council August 2026 Meeting Recap" (Aug 12, 2026)
  - "Clairemont Pool To Remain Closed Until Spring 2027" (Aug 12, 2026)
  - "Matcha Madness: 10 San Diego Spots to Get Your Fix" (Jul 29, 2026)
  - "The Local's Guide to Central San Diego Coffee Shops" (Jul 23, 2026)
  - "From 49 Subscribers to 7,200 Neighbors: One Year of Explore Clairemont" (Jul 15, 2026)

### Post Categories (21)

| Category | Posts (Aug 2026) | Was (Mar 2026) |
|---|---|---|
| Charity | 1 | 1 |
| Civil & Community | 17 | 8 |
| Fitness | 3 | 3 |
| Flashback | 4 | 2 |
| Guest Post | 2 | 2 |
| Kids & Family | 1 | 1 |
| Local | 3 | 0 |
| Local Biz | 20 | 16 |
| — Bakeries | 1 | 1 |
| — Bars | 3 | 3 |
| — Beer | 1 | 1 |
| — Coffee & Tea | 2 | 1 |
| — Desserts | 3 | 3 |
| — Restaurants | 6 | 6 |
| Meet Your Neighbor | 13 | 8 |
| Nature | 5 | 2 |
| Neighborhood Notes | 3 | 1 |
| Newsletter | 48 | 24 |
| Pets | 2 | 1 |
| Things to Do | 6 | 4 |
| Uncategorized | 0 | 0 |

The Newsletter category doubled from 24 to 48, matching the 48 Newsletter posts — that is one newsletter a week, consistently, for the whole period.

### Post Tags (34, was 31)
Asian Fusion, Barber shop (8), Beauty salon (23), Boxing, brunch, Candidates (2), Catholic, Christmas, contest, Cutest Pet Contestant (0), District 2 (2), Eyelash salon, Facial spa, Hair extension technician (6), Hair extensions supplier, Hair removal service, Hairdresser (9), Happy hour (2), history, library card, Make-up artist (2), Massage therapist, Microbakery, Nail salon (4), Organic shop, party, Pet Contestant (0), Santa, Service establishment, Steak, Stylist, `tanja@exploreclairemont.com` (0), Waxing, Waxing hair removal service (4)

New since March: Candidates, District 2, Microbakery, and one stray tag literally named `tanja@exploreclairemont.com` with 0 posts, which looks like an email address pasted into a tag field by accident and is safe to delete.

### Pages (97 total: 87 published, 9 drafts, 1 private)

Alphabetical, drafts and special pages marked:

About, Add Event Form (Draft), Add Event Form, Add Explorer Exclusives Form, Add Grin Gripe Gratitude, Add Listing Form, Add Reader Post, Add Review, Bay Ho, Bay Park, Birdland, Blog (Posts Page), Business Admin Dashboard, Business Admin Dashboard (Copy) (Draft), Checkout, Choose Adventure, Clairemont, Contact, Contest Entry Page, Contest Leaderboard, Contest Page, Customer Support, Directory, Disclaimer & Affiliate Policy, EC Feedback, EC Feedback, EC Review, Event Results, Events, Explore Clairemont (Front Page), Explore Clairemont-old (Draft), Explorer Exclusives, Fast Times Newsletter, Feedback Received, Feedback Received, Gather Locals Test Page, Giveaway, Grins Gripes and Gratitude, Kearny Mesa, Linda Vista, Listing Results, Log In, Login, Lost Password, McNeilly Insurance Partner, Member Directory, My Account (Draft), My Account, My Profile (Draft), My Punchcards, My Vouchers, Neighborhoods, No Vote, Order Confirmation, Order Failed, Partner, Partner Programs, People & Pets Of Clairemont, People Of Clairemont, Pets Of Clairemont, Pick Your Plan, Poll Thanks, Poll Vote, Privacy Policy, Promotions, Punch Card Activate, Punch Checkin, Punchcard Leaderboard, QR, QR Subscribe Page, Redeem, Refer-a-Friend, Reset Password, Reset Password (Draft), Resident Guide, Resources, Return Policy, Review Submitted, Serra Mesa, Sign Up, Sign Up-PP (Draft), Special Offers, Subscribe, Subscribe Landing Page, Subscribe Landing Page (Copy) (Draft), Subscribe Referral, Subscribe Test, Taco Trail Landing Page, Taco Trail Leaderboard, Terms of Service, test (Private), Test Check-In, Thank You (Draft), Thank You, The Local Scroll, Ticketing Dashboard, UGC Submission Form

New since March: Add Explorer Exclusives Form, Gather Locals Test Page, McNeilly Insurance Partner, My Punchcards, Poll Vote, Punch Card Activate, Punch Checkin, Subscribe Landing Page (Copy), Taco Trail Landing Page, Taco Trail Leaderboard, UGC Submission Form. The Taco Trail pages and the punch-card check-in pages are the visible half of the Punch Cards plugin build-out.

There are several near-duplicate pairs worth cleaning up eventually: two "EC Feedback", two "Feedback Received", "Log In" and "Login", "My Account" published and drafted, two "Reset Password".

### Comments (200 total)
- All (200) | Mine (58) | Pending (0) | Approved (200) | Spam (0) | Trash (0)
- Up from 90 in March. Still nothing in spam or trash, which is what you would expect when only logged-in registered users can comment.

### Listings (1,518 total, 1,513 published)
Business directory listings — the core content of the site. Custom post type with extensive taxonomies including Categories, Tags, Listing Types, and detailed feature groups (Health & Medical, Professional Services, Home Services, Shopping & Retail, Business Status, Food & Drink, General Features, Listing Statuses, Districts). Grew by 62 since March.

### Events (1,394 total, 1,353 published, 41 drafts)
Custom events post type with Categories, Tags, Event Types, Event Services, Entertainment Features, Food & Drink Features, Seating & Admission Features, and full ticketing/attendee management. **Doubled from 692 in March** — the event aggregator pipeline in the Events Calendar plugin is doing the work. 938 of the 1,394 are attributed to Tanja's account, which is what automated imports running under her user look like.

### Special Offers (8 total, 7 published, 1 draft)
Powered by EC Coupons Lite. Related content: 8 Business Packages (5 published, 3 drafts).

### Newsletters (48 published)
The Fast Times newsletter archive, one per week. Recent issues are titled in a subject-line style with emoji, for example "Matcha Madness + 3 Local Sites Eyed for Master Development" and "One Year Down + Local Eatery Unexpectedly Closes".

### Contest Entries (31 total, 28 published, 3 drafts)
Plus 1 published Contest. Managed by EC Contest.

### Punch Cards (1, in draft)
The Punch Cards plugin has ten admin sub-pages built out — UGC Submissions, Business Stats, Raffle Entries, Check-In Settings, Ledger Reconciliation, Flash Deal Settings, Flash Deal Submissions, Webhook Log — but only one punch card record exists and it is still a draft. The machinery is ahead of the content.

### Local Scroll Photos (21 approved, 0 pending)
Reader-submitted photos, all caught up with nothing waiting in the moderation queue.

### Other content types
- Reader Posts: 0
- Grins, Gripes and Gratitude: 1 published

---

## 8. USERS (2,783 total)

| Role | Count (Aug 2026) | Was (Mar 2026) |
|---|---|---|
| Administrator | 2 | 2 |
| Author | 2 | 1 |
| Contributor | 2,743 | 1,616 |
| Subscriber | 5 | 1 |
| Merchant | 30 | 8 |
| No role | 6 | 6 |

Contributors — registered community members — grew by 1,127 in five months, roughly 225 a month. **Merchants nearly quadrupled, from 8 to 30**, which is the more commercially interesting number: those are local business accounts.

The **Ad Admin** role that existed in March is gone. It came with Advanced Ads and left with it.

---

## 9. FLUENTCRM (Email Marketing)

| Metric | Value (Aug 25, 2026) | Was (Mar 22, 2026) |
|---|---|---|
| Active Contacts | 3,038 | 2,010 |
| Email Campaigns | 35 | 12 |
| Emails Sent (total) | 80,566 | 21,210+ |
| Active Automations | 1 | 2 |
| Tags | **125 (last checked March 2026)** | 125 |
| Email Templates | **2 (last checked March 2026)** | 2 |

Getting Started: still 4 of 5 steps complete (Create a Form is the outstanding one).

**Email performance (rolling window shown on the dashboard):** 12,457 sent, 12,457 delivered (100%), 6,245 opened (50.1%), 1,353 clicked (10.9%), 0 bounced.

**Recent campaigns:** Newsletter 08-20-26 (3,032 recipients, 48.61% open rate), Newsletter 08-13-26 (3,016 recipients, 50.99%), Newsletter 08-06-26 (3,016 recipients, 50.96%). A steady ~50% open rate on a 3,000-person list is unusually good and worth not breaking.

The one active automation is "New Subscriber Welcome Series".

---

## 10. EMAIL (FluentSMTP)

| Metric | Value (Aug 25, 2026) |
|---|---|
| Total emails logged | 6,265 |
| Active connections | 2 |
| Active senders | 1 |
| Email logging | On |
| Log retention | Delete after 14 days |

Deliverability remains clean — FluentCRM reports 0 bounces across 12,457 sends.

Note on comparing to March: the March file recorded "all time 4,846" but logs are pruned after 14 days, so the FluentSMTP total is a rolling figure, not a lifetime one. The lifetime send count to trust is FluentCRM's 80,566.

---

## 11. EC ADS (Ad Management)

**Advanced Ads is gone.** In March this site ran Advanced Ads, Advanced Ads Pro and Advanced Ads Tracking, plus two inactive Advanced Ads add-ons. All five have been uninstalled and replaced by **EC Ads 1.13.1**, an in-house plugin Tanja wrote. A commercial ad stack was swapped for one she owns and can change.

**Admin menu:** EC Ads → Analytics, Ads, Placements, Ad Groups, How to Use, Client Reports.

**Current ads (5, all published):**
- Canyon Villas Ad — Canyon Villas Retirement Community
- Canyon Villas Ad Cody — Canyon Villas Retirement Community
- Explorer Exclusives Cube
- Grow Your Business Box Form
- Little Backstube — Little Backstube

**Last 7 days, all ads combined:**

| Metric | Value |
|---|---|
| Renders | 6,654 |
| Times seen | 385 |
| Viewability | 5.8% |
| Clicks | 6 |
| Click rate | 1.56% |
| People (est.) | 194 |
| Times seen per person | 1.98 |

**By ad, last 7 days:**

| Ad | Business | Renders | Times seen | Viewability | Clicks | Click rate |
|---|---|---|---|---|---|---|
| Canyon Villas Ad | Canyon Villas Retirement Community | 4,300 | 255 | 5.9% | 6 | 2.35% |
| Grow Your Business Box Form | — | 2,354 | 130 | 5.5% | 0 | 0% |

**By device, last 7 days:** Mobile 58.4% of impressions (225 seen, 2 clicks, 0.89%), Desktop 36.1% (139 seen, 4 clicks, 2.88%), Tablet 5.5% (21 seen, 0 clicks). Most people are on mobile; the clicks come from desktop.

**How EC Ads counts things**, because the vocabulary is its own and easy to misread:
- **Renders** is how many times the ad markup was placed on a page. It is admin-only and advertisers never see it.
- **Times seen** is how many of those renders were actually viewed.
- **Viewability** is times seen divided by renders. A reading above 100% means something is wrong.
- **People (est.)** is what advertisers see instead of the raw placement count.

Three of the five ads recorded no activity in the last 7 days, so the live inventory is effectively two ads. The 5.8% viewability is low and probably worth investigating — it means most placements are rendering below the fold or in slots nobody reaches.

---

## 12. EC COUPONS / VOUCHER ANALYTICS

Data from the EC Coupons redemptions dashboard (Special Offers → Redemptions).

| Metric | Value (Aug 25, 2026) | Was (Mar 22, 2026) |
|---|---|---|
| Voucher records shown | 100 (see caveat) | 25 |
| Redeemed | 13 | 0 |
| Issued, not yet redeemed | 87 | 25 |
| Expired | 0 | 0 |
| Paid vouchers | 0 — everything is a free coupon | 0 |
| Total revenue | $0 | $0 |
| Merchant payouts | $0 (all rows Unpaid, face value only) | $0 |

**Caveat on the 100:** the dashboard renders exactly 100 rows with no pagination control, and the oldest row is dated Jan 22, 2026. That is almost certainly a hard cap rather than the true total, so read 100 as "at least 100". The redemption rate of 13% is calculated against what is displayed.

Active deal codes seen in the recent rows: VINYA_10 (Vinya: vino + vinyasa), UIC_20 (Unique Impressions Collective), LB_15 (Little Backstube), INDYA_APP (Indya).

The March note that the voucher system was going unused is now only half true — redemptions have started, but no voucher has ever carried a price, so the system still produces zero revenue and zero merchant payouts.

---

## 13. SITE REVIEWS

| Metric | Value (Aug 25, 2026) | Was (Mar 22, 2026) |
|---|---|---|
| Total reviews | 18 | 15 |
| Awaiting approval | 0 | 0 |
| Plugin version | 8.2.2 (by Paul Ryley) | 7.2.13 |

The March update warning is cleared; the plugin is on the 8.x line now. The admin menu offers an "Upgrade to Premium" link, so this is the free build.

---

## 14. MEDIA LIBRARY

| Folder | Files (Aug 2026) | Was (Mar 2026) |
|---|---|---|
| All Files | 1,425 | 1,150 |
| Uncategorized | 1,243 | 1,124 |
| Ads | 29 | folder did not exist |
| Icons | 0 | 0 |
| Logos | 130 | 1 |
| Marketing + Media Kit | 23 | 25 |

Folders are provided by Classic Monks (taxonomy `cm_media_folders`). The Logos folder went from 1 file to 130, which lines up with 30 merchant accounts and a growing listings directory. 87% of the library is still uncategorized.

Max upload size: 100 MB per file, up to 20 files per request.

---

## 15. FAST TIMES POLLS

48 polls exist in the manager, up from a handful in March. The format has changed: the newsletter now runs a recurring **House of the Week** poll where readers guess a home's sale price and the manager stores the correct answer, alongside occasional open questions.

**Most recent polls:**

| Slug | Heading | Votes | Created |
|---|---|---|---|
| house-08-27-26-4134-epanow | House of the Week Results | 0 (not yet sent) | Aug 24, 2026 |
| house-08-20-26-6093-camintodeleste | House of the Week Results | 115 | Aug 18, 2026 |
| house-08-13-26-3636-shawnee | House of the Week Results | 118 | Aug 11, 2026 |
| handyperson-08-06-26 | Do you have a handyperson/contractor you'd recommend? | 46 | Aug 5, 2026 |
| house-08-06-26-280-amulet | House of the Week Results | 101 | Aug 3, 2026 |
| house-07-23-26-4402-mtbigelow | House of the Week Results | 102 | Jul 28, 2026 |

Roughly 100 to 120 votes per House of the Week poll, against 59 votes on the March business poll. Engagement has roughly doubled, in line with the list size.

There is a duplicate slug pair — `handyperson-08-06-26` (46 votes) and `handyperson-088-06-26` (0 votes, created two days earlier) — clearly a typo that was re-created rather than fixed.

---

## 16. FULL ADMIN MENU STRUCTURE

The menu is now grouped with section separators added through ASE. The headings **CPTs**, **Fluent**, **Other Plugins** and **The Rest** are dividers, not real menu items.

1. **Dashboard** → Home, Updates
2. **Media** → Library, Add Media File, Folders
3. **Bricks** → Getting Started, Templates, Settings, Custom Fonts, Form Submissions, Sidebars, System Information, License, Next Bricks, Elements, AT License, Bricksable, AT Theme Settings
4. **Pages** → All Pages, Add Page
5. **Posts** → All Posts, Add Post, Categories, Tags, Districts

*— CPTs —*

6. **Newsletters** → All Newsletters, Add New Newsletter, Categories, Tags, Import Newsletters
7. **Listings** → All Listings, Add New Listing, Categories, Tags, Listing Types, Health & Medical Features, Professional Services Features, Home Services Features, Shopping & Retail Features, Business Status, Food & Drink Features, General Features, Listing Statuses, Districts
8. **Events** → All Events, Add New Event, Categories, Tags, Event Types, Event Services, Entertainment Features, Event Food & Drink Features, Seating & Admission Features, Business Status, General Features, Listing Statuses, Districts, Attendees, Settings, Webhook Logs, How It Works
9. **Special Offers** → All Special Offers, Add New Special Offer, Business Packages, Webhook Logs, Districts, Listing Types, Redemptions, Instructions, Settings, All Feedback
10. **Business Packages** → All Business Packages, Add New Business Package
11. **Punch Cards** → All Punch Cards, UGC Submissions, Business Stats, Raffle Entries, Instructions, Check-In Settings, Ledger Reconciliation, Flash Deal Settings, Flash Deal Submissions, Webhook Log
12. **EC Contests** → Contest Entries, Add New Contest Entry, Contest Categories, Instructions, Contests, Integrity, Contest Overview, Votes
13. **EC Ads** → Analytics, Ads, Placements, Ad Groups, How to Use, Client Reports
14. **Local Scroll** → Pending Photos, Add Photo, QR Code, QR Settings, Bricks Guide
15. **Fast Times Polls**
16. **Analytics** (EC Merchant Analytics — business analytics overview)

*— Fluent —*

17. **FluentCRM Pro** → Dashboard, Contacts, Lists, Tags, Campaigns, Recurring Campaigns, Email Sequences, Email Templates, Forms, Automations, Settings, Reports, Addons, Help, Companies
18. **FluentCommunity**
19. **FluentSnippets**
20. **Events Calendar** → Dashboard, Shortcodes, Run Cron
21. **Meta Box** → Dashboard, Post Types, Taxonomies, Custom Fields, Relationships, Settings Pages, Views, Extensions, Template, User Profile, License, Tools

*— Other Plugins —*

22. **Bit Flows Pro** → Dashboard, Flows, Connections, Webhooks, Custom Apps, Settings, License & Support, MCP Server, System Info, SMTP
23. **Bit Form Pro** → All Forms, Form Templates, App Settings, Integrations, SMTP, PDF Setting, CPT, Bit Form API, Payments, Doc & Support, License
24. **Classic Monks** → Classic Monks, Short Links, Logs, Media, Plugin, License, Menu
25. **Site Reviews** → All Reviews, Categories, Settings, Tools, Help & Support, Upgrade to Premium
26. **wpDiscuz** → Dashboard, Settings, Phrases, Tools, Addons, Forms
27. **WP Grid Builder** → Dashboard, All Grids, All Cards, All Facets, All Styles

*— The Rest —*

28. **Users** → All Users, Add User, Profile
29. **Plugins** → Installed Plugins, Add Plugin, Plugin File Editor
30. **Tools** → Available Tools, Import, Export, Site Health, Export Personal Data, Erase Personal Data, CDN Cache Purge, Enhancements, RentCast Shortcodes Help, Scheduled Actions, Import Newsletters, Debug Log Manager
31. **Appearance** → Themes, Patterns, Widgets, Menus, Theme File Editor, Customize, Fonts
32. **Settings** → General, Writing, Reading, Discussion, Media, Permalinks, Privacy, Admin Menu, Admin Columns, Favorite Posts, Redis, Slim SEO, Perfmatters, FluentSMTP, Connectors
33. **Comments**
34. **Reader Posts** → All Reader Posts, Add New Reader Post, Categories
35. **Grins Gripes and Gratitude** → All Entries, Add New, Categories, Tags
36. **Bracket Manager** (EC Bracket)
37. **Relevanssi** → Settings, User searches, Admin search

Changes since March: Advanced Ads is gone and EC Ads is in its place; Bracket Manager is new; Local Scroll and Fast Times Polls moved up into the CPTs group; Relevanssi is now its own top-level menu instead of living under Dashboard; Debug Log Manager appears under Tools; Punch Cards gained five sub-pages; Bit Flows Pro gained an MCP Server page.

---

## 17. KEY OBSERVATIONS & NOTES

1. **The site is now more in-house than off-the-shelf.** Eleven of 44 active plugins are Tanja's own code, and the biggest change since March is that the commercial ad stack (Advanced Ads plus Pro plus Tracking plus two add-ons) was ripped out and replaced by **EC Ads 1.13.1**, written in-house. Three more custom plugins are new since March: EC Ads, EC Bracket and The Local Scroll.

2. **The events pipeline is the standout success.** Events went from 692 to 1,394 in five months. That is automated aggregation working, not manual entry — 938 of them sit under Tanja's user account, which is the signature of an importer running as her.

3. **The audience grew about 70%.** 1,632 users to 2,783, driven by Contributors (1,616 to 2,743). Merchants nearly quadrupled, 8 to 30. FluentCRM contacts went 2,010 to 3,038 with campaigns 12 to 35 and lifetime sends 21,210 to 80,566, all at a ~50% open rate and zero bounces.

4. **Maintenance is in much better shape than in March.** Zero pending updates across core, plugins and themes. Zero inactive plugins. Both March critical Site Health issues are resolved — the Bricks theme is current and debug logging is off. What remains is one performance critical ("page cache detected but server response is still slow") and the same late-cron warning that was there in March.

5. **The database is the thing to watch.** It doubled, 858 MB to 1.71 GB, and total footprint went 4.27 GB to 5.49 GB. Uploads also jumped from 597 MB to 865 MB. The PHP opcode cache is reported as **full** (128 MB of 128 MB, interned strings 100% of 8 MB with 24 bytes free), which is a plausible contributor to the slow server response flagged by Site Health.

6. **Search indexing was turned on.** In March the site was set to discourage search engines. It no longer is. If anyone is wondering why organic traffic patterns changed, that is the switch.

7. **Ad viewability is low.** 6,654 renders produced only 385 views in the last 7 days — 5.8%. Only two of five ads recorded any activity. Mobile carries 58% of impressions but desktop produces two-thirds of the clicks.

8. **Vouchers still make no money.** Redemptions have started (13 of at least 100 records), but every voucher is a free coupon, so revenue and merchant payouts are both $0. The monetisation path exists in the plugin and has never been used.

9. **Punch Cards is built but not launched.** Ten admin sub-pages including ledger reconciliation and flash deals, plus five front-end pages, against exactly one punch card record which is still a draft. The plugin is also still on a release candidate version.

10. **Small cleanup items.** A post tag named `tanja@exploreclairemont.com` with 0 posts; a duplicated poll slug (`handyperson-08-06-26` vs `handyperson-088-06-26`); several near-duplicate pages (two EC Feedback, two Feedback Received, Log In vs Login, two Reset Password); 1,243 of 1,425 media files still uncategorized. None of these break anything.

11. **Auto-updates are disabled everywhere** — all 44 plugins and both themes. Updates are current today because someone ran them, not because the site keeps itself current. This is worth a recurring calendar reminder.

---

## APPENDIX: WHAT COULD NOT BE VERIFIED

These figures are carried over from the March 22, 2026 audit and were **not** re-confirmed on August 25, 2026, because reading them would have required interacting with a settings screen:

- FluentCRM **Tags: 125** and **Email Templates: 2** — the FluentCRM admin is a single-page app whose tag route would not load read-only.
- The FluentSMTP per-period sent/failed breakdown (today / 7 days / all time). Only the rolling "Total Email Sent (Logged): 6,265" figure was readable, and logs are pruned after 14 days.
- EC Merchant Analytics aggregate numbers. That dashboard requires selecting an individual business before it shows anything, so there is no site-wide total to quote.

Treat all four as unknown rather than current.
