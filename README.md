# Clairemont Context — Master Reference

Background files about Tanja, ExploreClairemont.com, and everything around it, written to be loaded at the start of an AI session so the assistant already knows the business.

**Last refreshed:** 25 August 2026

> These files are for Claude. The Explore Clairemont Custom GPT has its own operating instructions in `ec-integrations-api/docs/GPT_INSTRUCTIONS.md`, which cover which API tool to call when. Different assistant, different job. Don't merge the two.

---

## Files in this repository

| File | What it covers |
|---|---|
| `about-tanja.md` | Who Tanja is, how she works, how she wants things explained |
| `exploreclairemont-site.md` | The site itself — sections, features, mission |
| `brand.md` | Colors, font, logo usage |
| `tone-and-voice.md` | Voice guide, with examples of what sounds right and what doesn't |
| `fast-times-newsletter.md` | The newsletter — format, structure, conventions |
| `instagram.md` | @exploreclairemont — stats, content style, highlights |
| `business-development.md` | Sales playbook, audience data, partnership products and pricing |
| `resident-guide.md` | The 62-page Resident's Guide lead magnet and neighborhood data |
| `ec-store-overview.md` | store.exploreclairemont.com and everything sold there |
| `ec-wordpress-setup.md` | Full WordPress audit — plugins, content counts, server, admin structure |
| `tools-and-integrations.md` | The third-party stack |
| `projects.md` | Every GitHub repo and local project, what each does, where the current version lives |

---

## Quick reference

**Site:** ExploreClairemont.com
**Store:** store.exploreclairemont.com
**Newsletter:** Fast Times, weekly, always opens with "Hey Neighbor!"
**Social:** @exploreclairemont on Instagram, Facebook, TikTok
**Neighborhoods:** Clairemont, Linda Vista, Bay Ho, Bay Park, Kearny Mesa, Serra Mesa, Birdland
**Zip codes:** 92110, 92111, 92117, 92123
**Platform:** WordPress, Bricks Builder, Meta Box, FluentCRM
**Operator:** Tanja — Clairemont native, Mountain Streets resident, vibe coder
**GitHub:** github.com/sportyspice7

**Current scale (August 2026):** 3,100 newsletter subscribers, 4,700 Instagram followers, 1,518 listings, 1,394 events, 2,783 registered users

---

## How to use these files

### In Claude Code
```
/add-file README.md
/add-file about-tanja.md
/add-file exploreclairemont-site.md
/add-file brand.md
/add-file tone-and-voice.md
/add-file fast-times-newsletter.md
/add-file instagram.md
/add-file business-development.md
/add-file resident-guide.md
/add-file ec-store-overview.md
/add-file ec-wordpress-setup.md
/add-file tools-and-integrations.md
/add-file projects.md
```

For most conversations you won't want all of them. Sensible smaller sets:

- **Writing anything** — `about-tanja`, `tone-and-voice`, `fast-times-newsletter`, `brand`
- **Sales or partnerships** — `about-tanja`, `business-development`, `ec-store-overview`, `resident-guide`
- **Plugin or site work** — `about-tanja`, `ec-wordpress-setup`, `projects`, `tools-and-integrations`
- **Social content** — `about-tanja`, `tone-and-voice`, `instagram`, `brand`

### In Claude Web, Desktop or Cowork
Attach the files directly, or paste this at the start:

> Please read all the files in my ec-context repo before we begin. They contain full context about me, my site ExploreClairemont.com, my newsletter Fast Times, my brand, and my content voice.

---

## Keeping this current

Every file that carries numbers should say when they were checked. If a figure has no date next to it, treat it as unverified.

| When this changes | Update this |
|---|---|
| Follower or subscriber counts | `instagram.md`, `business-development.md`, and the Quick Reference above |
| A plugin is installed, removed or updated | `ec-wordpress-setup.md` |
| A new repo or project appears | `projects.md` |
| Site features or sections change | `exploreclairemont-site.md` |
| Pricing or partnership products change | `business-development.md` |
| Newsletter format changes | `fast-times-newsletter.md` |
| Voice shifts | `tone-and-voice.md` |
| A new tool joins the stack | `tools-and-integrations.md` |

Two figures that have contradicted each other in the past are the Instagram follower count and the newsletter subscriber count, because they appear in more than one file. When either changes, search the whole repo for the old number rather than editing one file.
