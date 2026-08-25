# Projects — every repo and local project

What Tanja has built, what each piece does, and where the current version of it actually lives.

This file exists because the same plugin can sit in three places at once — the live site, GitHub, and her Mac — at three different versions. When an assistant is asked about a plugin, this tells it which copy is the truth.

---

## How to read this

Any given project can exist in three places, and they do not always agree:

- **Live** — running on exploreclairemont.com right now
- **GitHub** — the repo under `github.com/sportyspice7`
- **Mac** — the working folder, normally under `Documents/GitHub`

When those three disagree, the newest one is not automatically the right one. A version sitting on your Mac may be unfinished, and a version on GitHub may be a year stale. Every entry below says plainly which copy is the truth.

---

## Where things stand today

| Project | Live | GitHub | Mac | Status |
|---|---|---|---|---|
| EC Ads | 1.13.1 | 1.13.1 | 1.13.1 | In sync |
| EC Coupons Lite | 1.6.0 | 1.6.0 | 1.6.0 | In sync |
| Fast Times Poll Manager | 1.8.2 | 1.8.2 | 1.8.2 | In sync |
| General Reviews | 1.2.0 | 1.2.0 | — | In sync |
| The Local Scroll | 1.22 | 1.22 | — | In sync |
| EC Contest | 1.7.5 | 1.6.0-dev | 1.6.0 | GitHub behind |
| EC Merchant Analytics | 2.0.9 | 1.8.0 | 2.0.9 | GitHub behind |
| Punch Cards | 1.0.0-rc83 | 0.2.0 | 1.0.0-rc85 | GitHub badly behind |
| EC Events Ticketing | 1.1.0 | 1.1.0 | 1.2.0 | Mac ahead, uncommitted |
| Events Calendar | 1.3.1 | 1.3.1 (zips only) | 2.0.0 | Mac ahead, unmerged branch |
| EC Bracket | 1.3.0 | *empty repo* | Desktop folder | **Not backed up in git** |
| RentCast Shortcodes | 1.2.0 | *no repo* | *not found* | **Live only** |

---

## The shared foundation

Nearly every WordPress plugin here sits on the same five pieces. Knowing them explains most of the dependencies.

**Meta Box** — custom fields. Almost every plugin reads its data through `rwmb_meta()`. If Meta Box is off, most of these break. The Local Scroll is the one exception.

**Bricks Builder** — the page builder. Several plugins register dynamic tags so their data can be dropped into a Bricks template.

**FluentCRM** — the email and audience system behind the Fast Times newsletter. Contests, polls and coupons all tag people into it.

**Zylvie** — the external checkout. Coupons, punch cards and ticketing all receive Zylvie webhooks when someone buys something.

**Site Reviews** — the review engine that General Reviews wraps.

---

## Gather Locals

A separate business from Explore Clairemont. Worth stating clearly, because the naming invites confusion and even the AI briefing docs have to spell out the distinction.

### gather-locals-app
The live product. A multi-tenant Laravel SaaS where community organizers each get their own subdomain to run local gatherings — signups, payments, small-group matching, messaging, venues and ticket sales. Around 318 PHP classes, 340 tests, real production deploys. Actively developed, with commits landing daily.

**Truth: GitHub.** This is the healthiest repo in the account and its README is genuinely well maintained.

### gather-locals
An archive. One zip of the WordPress plugin (v2.4.7) that the Laravel app replaced, plus handoff notes. Frozen since April 2026.

**Truth: nothing to maintain.** Keep for reference, archive on GitHub.

---

## Explore Clairemont — the revenue plugins

These are the ones that make money, and they are the most developed.

### ec-ads
A self-hosted ad server. Create ads, create placements, and the plugin decides which ad appears where, counts who saw and clicked it, and emails each advertiser a performance report. Targeting by post type, taxonomy, URL, device, user role, referrer source and more. Real A/B testing with a nightly cron that shifts weight toward the better performer once there is enough data.

Impressions only count when at least half the ad is on screen for a full second, bots are filtered by user agent, and data is kept for 90 days. Those rules matter because advertisers ask about the numbers.

**Truth: all three agree at 1.13.1.** Note that 1.12.0 and 1.13.0 were never packaged as zips, and nobody has looked at the newer dashboards on a screen yet.

### ec-coupons-lite
The Explorer Exclusives voucher system. An offer is published, a customer claims or buys it through Zylvie, they get a voucher with a unique key, the merchant redeems it at the counter, and the plugin then emails a tokenized link asking for a review. Merchants get their own dashboard with redemption counts and payouts.

**Truth: all three agree at 1.6.0.** The repo is cluttered — six committed zips, a nested duplicate directory, two legacy copies of the old single-file version.

### ec-punchcards
Digital punch cards. A resident collects a card, visits participating businesses, scans a QR code at each one, and finishing the card earns raffle entries.

This one needs the most explanation. GitHub is stranded at **0.2.0 from December 2025**. Your Mac has **1.0.0-rc85**, the product of a serious security rebuild across 85 release candidates, sitting on a branch called `codex/secure-rebuild` that was never merged. The live site runs **rc83**.

The rebuild added signature-verified and encrypted Zylvie webhooks, a proper deduplicated activity ledger, opaque QR codes that no longer leak identifiers, hashed single-use sign-in links, seven check-in verification methods, Flash Deals, and real privacy work. rc84 and rc85 split the Zylvie secret into separate lead and sale secrets.

**Truth: the Mac, on that branch.** But read the deployment warning at the bottom of this document before pushing it anywhere.

### ec-events-ticketing
Ticket sales and door check-in. A Zylvie purchase fires a webhook, the plugin generates a unique code and QR image and emails the ticket, and staff scan it at the door. A code can only be used once. Its README is the best-written document in the account.

**Truth: the Mac at 1.2.0**, which adds multi-ticket orders so one purchase can cover several admissions. The code is finished and its tests pass, but it is uncommitted work on a feature branch.

### EC-Contest
Photo voting contests. People vote with their email and must click a confirmation link before the vote counts. One vote per email per category. Anti-fraud comes from a honeypot field, IP rate limiting, disposable email blocking and an integrity dashboard.

44 shortcodes, which is why an accurate README matters here more than anywhere else.

**Truth: the live site at 1.7.5.** GitHub is at 1.6.0-dev and is missing the generic entry-detail fields that replaced the pet-specific ones, plus public entry submission.

---

## Explore Clairemont — the content pipeline

### ec-event-aggregator
A Python pipeline that visits around 25 San Diego venue websites and calendars, extracts upcoming events, removes duplicates, hands you a spreadsheet to prune, then publishes what survives into WordPress as drafts. Run weekly, by hand, on purpose.

Its safety rules are the important part. It only ever creates drafts, never updates an already published post, and deliberately refuses to write the date fields that the calendar plugin computes. The design philosophy in its own words: the scraper prepares events, humans approve, the calendar plugin computes dates.

**Truth: GitHub and the `EC Event Aggregator` folder agree.**

### events-calendar
Works out every actual date an event happens. Events can be a single day, several days in a row, a scattered set of custom dates, or a repeating pattern like the first and third Tuesday. The plugin flattens all of that into concrete date lists so page templates just read a value.

**Truth: the Mac at 2.0.0**, on an unmerged branch. GitHub's main branch holds nothing but two zip files, which is why it displays as an empty repo. Live runs 1.3.1. The 2.0.0 work is a security and performance refactor with no functional changes, so the shortcodes are identical.

### the-local-scroll
Community photo sharing. Someone scans a QR code on a poster, uploads a neighborhood photo from their phone, and it lands in a moderation queue. Approved photos appear in a Bricks gallery. First-time uploaders get a WordPress account created automatically.

**Truth: GitHub at 1.22.**

### General-reviews
Site Reviews can only attach a review to a business that already exists in the directory. This wraps it in a three-step flow so a visitor can search for a business, add it if it is missing, and then review it. New businesses arrive as drafts for you to approve.

**Truth: GitHub at 1.2.0.** Ships two ways, as a plugin and as Fluent Snippets, and those two versions have drifted apart.

### fast-times-poll-manager
Newsletter polls where the click *is* the vote. Each answer option becomes its own link with the subscriber's email merged in, so there is no form to fill in. Supports single choice, multiselect and guess-the-price quizzes, with free-text follow-ups you can reply to by email.

**Truth: all three agree at 1.8.2.**

### newsletter-post-converter
Turns a sent Fast Times newsletter into a draft post so the newsletter also lives on the website as an archive. Deliberately a button rather than an automatic hook.

**Not a plugin.** It is a single file meant to be pasted into Fluent Snippets, which is an easy thing to get wrong.

**Truth: GitHub.** No version is declared anywhere, which is worth fixing.

### EC-Analytics-Dashboard
Tracks how many people viewed each business listing and whether they clicked through to the phone, website or directions. Businesses see their own numbers, you see everything.

The attribution is the clever part. Event views get credited to the venue business, special offer views to every related listing, and blog post views to any business tagged in the Businesses Mentioned field.

**Truth: live and the Mac agree at 2.0.9.** GitHub is at 1.8.0. Between those versions came bot filtering, new-versus-returning visitors, UTM traffic sources, and a fix for the CDN stripping the session cookie and making every cached page load look like a new visitor.

---

## The AI layer

### ec-integrations-api
A FastAPI service on Google Cloud Run that lets the Explore Clairemont Custom GPT read Gmail, Google Drive, the NinjaPipe CRM and GitHub. It exists because the previous WordPress-based bridge hit size limits, including a media kit PDF it could not extract.

The boundaries are deliberate. Gmail creates drafts but has no send endpoint. Drive is read only. CRM deals are read only while contacts and companies can be written. GitHub is read only. The OAuth handling is genuinely well built, with signed expiring state and refresh tokens written straight into Secret Manager rather than to disk.

**Truth: GitHub at 0.6.0.** Its README describes everything as "planned" when it is all shipped and working.

### ec-context
Briefing documents written for an AI assistant rather than for a person. Load them at the start of a session and Claude already knows the business, the voice, the tools and the numbers.

**Truth: GitHub**, though the local copy on the Desktop is behind. Needs a refresh. Its own README indexes only 4 of the 10 files it contains, and the Instagram follower count contradicts the business development document because they were written months apart.

---

## Projects with no GitHub repo

Real work living only on the Mac, in the Desktop folder. Each of these is one hard drive failure from gone.

### ec-bracket
**Live on the site at 1.3.0.** Monthly Best of Clairemont tournament brackets for newsletter subscribers. Eight or sixteen competitors over three or four rounds, one round per newsletter send, with the subscriber's email merged into the vote link so there is no form to fill in. Also has a per-subscriber comment box that the plugin description does not mention.

Round advancement is manual, by design. You press Close Round and Advance Winners, and it refuses to run if any matchup is tied or has no votes so you can settle those by hand first. A monthly bracket costs three or four newsletter sends plus a manual close between each.

The build plan document in that folder describes a completely different plugin, using Supabase and browser fingerprinting. None of that was built. Read it as history, not documentation.

### News Aggregator
Weekly news gathering for Fast Times. Pulls the last seven days from 25 RSS feeds, 9 Reddit sources, 43 Google News queries and six hand-written scrapers covering Inside San Diego, city planning notices, four planning group agendas, the police and fire departments and two council district offices. Filters on neighborhood keywords, removes near-duplicate headlines, then has Claude write a two-sentence blurb for each. The output is a review queue, not finished copy.

Note that its `SETUP.md` describes a Google service account, which is wrong. The code actually uses ordinary OAuth sign-in.

### sd-council-scraper
Pulls City Council meeting transcripts, scans for eight neighborhood names, and has Claude both summarize the meeting and judge whether each keyword hit is genuine or a false positive. The Bay Park versus Mission Bay Park problem is written into the prompt.

This one is quietly the most valuable thing in the folder. It surfaces stories nobody else is reporting, because they were only ever said out loud in a room.

### neighborhood-lead-scrapers
Five Python scripts pulling public permit and licence data, feeding both editorial coverage and ad sales leads. No credentials needed, all public datasets.

The liquor licence script handles the new-versus-renewed problem properly. For each licence it opens the detail page and checks whether it came from a prior licence number, tagging each row as a new licence or a transfer and naming the previous business. The county food permit script only partly handles it, and a change of ownership still reads as new.

The three sources chain over time, which is the useful part. A restaurant build-out permit appears months before a liquor licence filing, which appears before the health permit with the real business name. A business turning up across several files is the strong signal.

### promotion-system
Badge and expiry management for business listings. Seven PHP snippets plus three Meta Box field group exports, meant to be pasted into Fluent Snippets rather than installed as a plugin. The whole model is one rule: every promotion type is a yes/no flag plus an expiry date, and the badge shows only when both hold.

Two real defects found. The contest field names in the JSON export do not match what the sync file reads, so contests may always look active. And the listing status taxonomy slug is written two different ways across the files.

### RentCast Shortcodes
Live on the site at 1.2.0, source not located anywhere. Worth downloading from the plugins page.

---

**Before any of these become repos:** News Aggregator holds `.env`, `client_secret.json` and `token.json`, and sd-council-scraper holds `.env`. A `.gitignore` protecting all of them is now in place in each folder. It has to stay there.

---

## Empty repos

Named on GitHub, no files in them.

- **bracket-maker** — the code exists on the Desktop and is live on the site
- **news-aggregator** — the code exists on the Desktop
- **business-raffle** — no code found. The raffle feature it describes is already built into ec-punchcards.

---

## Superseded

Safe to archive on GitHub. Nothing here needs maintaining.

- **EC-Punch-Cards** — the December 2025 version, replaced by `ec-punchcards`. Note the spelling difference, it is the whole reason these got confused.
- **gather-locals** — replaced by `gather-locals-app`
- **wp-event-aggregator** — not yours. An untouched fork of a Xylus Themes plugin. The name sits three characters from `ec-event-aggregator` and has nothing to do with it.

Local copies of superseded work now live in `Documents/GitHub/_archive/`.

---

## Things worth fixing

Roughly in order of how much they matter.

### Credentials
1. A Google Maps API key is hardcoded in `General-reviews` source. Rotate it and add a referrer restriction so it only works from your domain.
2. A WordPress application password and an Anthropic API key are in `ec-event-aggregator`'s git history. Removing a line from a file does not remove it from history, so rotating the credentials is the only real fix.

### Backup
3. Get `ec-bracket` into its repo. It is live on your site and backed up nowhere.
4. Get `News Aggregator` into its repo, with a `.gitignore` first so the `.env` file stays out.
5. Find the RentCast plugin source, or download it from the live site.

### Before deploying punch cards rc85
The rebuild changed QR code URLs to opaque codes and turned the old format **off** by default, behind a setting called `EC_PUNCHCARDS_ENABLE_LEGACY_QR`. Any QR code already printed and sitting at a business would stop working. The plugin's own `COMPLETE.md` says rc85 is code-complete for staging and explicitly not production ready, and its acceptance test checklist is entirely unticked. Staging first.

### Documentation drift already fixed in the new READMEs
Several old READMEs documented shortcodes that do not exist, which prints literal text on the page instead of the thing you wanted. The worst offender was ec-punchcards. All shortcode names in the new READMEs were verified against the actual code.

### Smaller bugs found along the way
- **ec-coupons-lite** — the Redemptions screen's own links use underscores while the menu registers hyphens, so the CSV export and Clear links land on a permissions error. Three feedback files are never loaded, so `[ec_private_feedback]` does nothing while an admin page for it still appears.
- **the-local-scroll** — the five-per-day rate limit is written but never actually called.
- **EC-Analytics-Dashboard** — phone number clicks on ordinary `tel:` links are not being recorded.
- **ec-events-ticketing** — event capacity is calculated but never enforced.
- **events-calendar** — a standing weekly event silently runs out of dates about a year after its start date and marks itself expired until someone re-saves it.
- **fast-times-poll-manager** — a stale duplicate file sits in the repo whose header contradicts its own filename.

---

## Naming rules going forward

1. **Local folder names match GitHub repo names exactly**, spelling and hyphens included. `ec-punchcards` is one word. `EC-Punch-Cards` is the dead one.
2. **One home for code.** `Documents/GitHub`. Not the Desktop, not two places.
3. **Superseded copies go to `_archive/`** with a version and date in the name, so you never have to open one to know what it is.
