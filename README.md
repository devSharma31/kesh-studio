# Kesh Studio — salon landing page (concept)

A mobile-first landing page for a fictional unisex hair and beauty salon in Kothrud, Pune. It's built around one action: **book a slot on WhatsApp with the service and time already filled in.**

**Live:** [kesh-studio-two.vercel.app](https://kesh-studio-two.vercel.app) · [GitHub Pages](https://devsharma31.github.io/kesh-studio/)

> Concept project for my design portfolio. The business, prices, ratings, address and phone number are fictional, and the reviews are labelled as samples.

---

## The brief

| | |
|---|---|
| **Business** | Unisex hair & beauty salon, mid-range |
| **Customers** | Working professionals and college students, 20–40, who book by phone |
| **Goal** | Book a slot on WhatsApp, with service and preferred time prefilled |
| **Brand feel** | Fresh, calm, professional |

## The real problems, and how the page solves them

| Problem | Fix on the page |
|---|---|
| **The owner misses calls while working on clients**, so people book elsewhere | A booking form in the hero builds the WhatsApp message for you: pick service, day and time, tap once. "Reply within 10 minutes" is stated upfront. |
| **Customers don't know prices before arriving** | A full price list right after the hero, GST included, with time per service. The headline reads "The price you see is the price you pay". |
| **Frequent no-shows** | A reminder the evening before, free rescheduling up to 2 hours before, and a ₹200 refundable token only for long colour and keratin slots, explained so it feels fair. |

## Design decisions

- **Section order follows the customer's questions:** book (hero) → *how much?* (prices) → *is it a hassle?* (3 steps) → *can I trust it?* (hygiene and policy) → reviews → location and hours → FAQ → final CTA.
- **Colour:** off-white `#F7F5F0`, ink `#1D2725` (14:1 contrast). **Teal `#0B5F55` is used only on buttons** (7.5:1 with white text), so anything teal is something to tap.
- **Type:** Fraunces for headings (calm, premium) and Inter for body text (readable on small screens).
- **Mobile-first:** designed for a 375px phone first. A sticky Call + WhatsApp bar stays visible on mobile.

## Conversion review (second pass)

I reviewed the first version from two sides: a busy customer on a phone with a slow connection, and the owner who wants more bookings.

| Issue found | Change |
|---|---|
| Main CTA was **below the fold** (ended at 878px on a 375×667 screen) | Merged six day/time chips into two dropdowns, removed a badge, shortened the intro. **The button now ends at 581px.** |
| Sticky button sent a prefilled booking ("Haircut — Men, Today, Morning") even if the visitor chose nothing, so the owner got bookings nobody picked | Sticky and final buttons send blank fields until the visitor makes a choice |
| Instagram and YouTube cards mid-page pulled visitors away before booking | Social links moved to the footer; mid-page shows ratings only |
| Google Fonts blocked the first paint on slow connections | Fonts load in the background; text shows immediately in a system font |
| Generic copy ("Ready for a fresh look this week?") | Replaced with specific lines ("After-work slots fill up by Thursday") |

## Accessibility and performance

- Semantic HTML, labelled form controls, keyboard-accessible service tabs, visible focus ring
- All text passes WCAG AA contrast
- Images below the hero are lazy-loaded, with a styled fallback if an image fails
- No frameworks: one HTML file with inline CSS and about 40 lines of JavaScript
- SEO: meta description, Open Graph tags, and `HairSalon` JSON-LD structured data

## What I'd test next with real customers

1. **Hero form vs a single "Book on WhatsApp" button.** Does the extra step lower taps but raise confirmed bookings?
2. **The ₹200 token.** Does it cut colour/keratin no-shows, or put people off booking?
3. **Message drop-off.** How many people open WhatsApp but never press send? Track it with a reference code in the message.

## Stack

HTML · CSS · vanilla JavaScript · Google Fonts · Unsplash photos · Simple Icons (CC0) · deployed on GitHub Pages and Vercel

## How this was built

I built this with Claude (Anthropic's AI assistant) as a design and coding partner.

**My part:** I wrote the business brief and page requirements, reviewed every version, asked for revisions (verified photos, menu images, real brand logos), commissioned the conversion review above, and published the site to GitHub and Vercel.

**Claude's part:** it wrote the HTML, CSS, JavaScript and copy to that brief.

---

Concept design by Devashish Sharma. Fictional business.
