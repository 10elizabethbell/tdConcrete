# TD Concrete — handoff at ~60%

**Live:** https://10elizabethbell.github.io/tdConcrete/ · **Repo:** https://github.com/10elizabethbell/tdConcrete · **Built:** 2026-10-20 from Muse brief (run 2026-10-21, Facebook group "Essex County Contractor Referrals") · On the Call Sheet: yes

## What's built
- **One page, calm band style:** paper header (drawn "TD" mark + wordmark, `519-796-7967` tap-to-call top right) → hero → services (8 rows on navy) → three service photo cards → "We treat your property like it's ours." care list → How it works (3 steps, deep navy) → quote form → "Call today for a quote." closing band with the big number → footer.
- **Hero:** eyebrow "Excavating & concrete", H1 "Dug, graded and poured in **Essex County.**" (letter bounce-in), promise "We come out, look at the job with you, and give you a straight quote.", buttons **Get a quote** (amber, to the form) and **See what we do** (outlined, to the services). On phones the copy sits on deep navy and the driveway photo shows below the buttons; on desktop the photo fills the band under a left-to-right navy fade.
- **Palette:** paper `#f4f6fb`, slate navy `#1f3d5a`, deep navy `#102234` (faint line texture), **machine amber `#f2a93b`** as the one accent (fills only; `#8a5200` when it's text on light). Form hover/focus outline blue `#1f5fa8`.
- **Contact wiring:** every service row and photo card jumps to the form and pre-selects that job. The form needs a job (chip or a few words) and a name, then opens a pre-written text to 519-796-7967. If no messages app opens, it shows the message with **Copy message**, **Open in Messages** and the number to call. The floating text circle appears after the hero and hides at the form. The form also says "Rather talk? Call 519-796-7967."
- **Motion:** H1 bounce-in, `.rise` fade-up, floating circle. Under reduced motion and without JS everything shows at once (checked).
- **Link preview / icons:** `og.jpg` (1200x630, hero photo + name + headline), `favicon.svg`, `apple-touch-icon.png` — all from my "TD" lettering, since there's no logo. Sources in `tools/`.

## Images
None of these are TD Concrete's jobs. They're shown as examples of each service, with no "our work" or "recent projects" label anywhere.

| File | What it shows | Source | Licence |
|---|---|---|---|
| `img/hero.webp`, `img/hero-phone.webp` | fresh grey gravel driveway up to a red-brick bungalow, flat Ontario farmland | generated with gpt-image-1, 2026-10-20 ("real-estate photograph … crushed grey limestone gravel driveway … red-brick ranch-style bungalow … southwestern Ontario") | generated; OpenAI terms assign output to the user |
| `img/excavating.webp` | excavator beside a fresh foundation dig | generated with gpt-image-1, 2026-10-20 ("residential excavation pit for a new house foundation … unbranded excavator") | same |
| `img/concrete.webp` | broom-finished concrete patio, forms still on, evening light | generated with gpt-image-1, 2026-10-20 ("freshly poured broom-finished grey concrete patio slab …") | same |
| `img/grading.webp` | backyard graded flat with dark topsoil, compact track loader | generated with gpt-image-1, 2026-10-20 ("large backyard freshly graded with dark screened topsoil …") | same |
| `og.jpg`, `favicon.svg`, `apple-touch-icon.png` | link card and "TD" mark | made for this site (`tools/og.html`, `tools/icon.html`) | ours |

Full prompts are in `~/.local/share/genimg/log.jsonl`; originals in the ignored `src-assets/gen/`.

## Assumptions I made
- **Voice "we":** "FULL EXCAVATING & CONCRETE SERVICES" reads like a crew. Switch to "I" if it's one person.
- **Colours:** no logo or brand exists, so the amber comes from the trade (excavators, safety gear) and the navies from the house style.
- **H1 place:** "Essex County" (the group they posted in, and the 519 area code). No towns are confirmed; the form's placeholder names Essex, Kingsville and Harrow as examples only.
- **Service labels** are shortened from their ad (e.g. "Sand, Stone Fill & Broken Concrete Removal" → "Fill & concrete removal"; "Parking Lots & Large Projects" → "Parking lots & large jobs").
- **Care promises** ("We walk the job with you first", "Graded so water runs away from your house", "Cleaned up before we leave") and the steps ("We come and look. Then you get a straight quote.", "And leave it clean.") are written as commitments. The owner must confirm each is true for them.
- **Spelling:** Canadian (`lang="en-CA"`); phone shown as they write it, 519-796-7967.

## Placeholders and gaps
- **Their own trust claims are on the page but hidden** (`#adClaims` in the care section, with a comment): "35+ years of hands-on experience", "Fully insured", "Locally owned & operated". The brief marks them unverified and says not to publish them as fact. Remove `hidden` once the owner confirms; they're the strongest hook in their ad.
- **Texting is unconfirmed.** The form, the text circle and "Open in Messages" all send to 519-796-7967. If it's a landline, texts vanish silently: switch the circle to `tel:` and the form button to "Call to send this", or set `CONFIG.SMS` to a mobile.
- **No email** (so no footer email), **no Facebook business page** (so no "see more of our work" link under the photos and none in the footer). The ad came from a personal profile whose role is unknown; I didn't link or name it.
- **No real photos, logo, hours, reviews, prices or owner name.** Nothing about them is on the page.

## Questions for the owner
1. Can 519-796-7967 take texts? If not, is there a mobile number for quote texts?
2. Can we say "35+ years", "fully insured" and "locally owned & operated" on the site?
3. Photos of real jobs (driveways, digs, pours), ideally wide and landscape, to replace the examples.
4. Which towns do you cover, and do you go into Windsor / Chatham-Kent?
5. Is there a logo, a truck lettering or colours you use?
6. A business email and Facebook page to put in the footer?
7. Who's the contact name customers will deal with, if you'd like it on the site?
8. Hours, and do you do winter work / snow?

## Ideas not built (yours to pick)
- **Signature motion (opt-in), trade worlds:** (1) **drag to grade**: a grader blade the visitor drags across a rutted gravel driveway, leaving it smooth and crowned (best fit: it's their most-listed job); (2) stone pouring off a tailgate into a pile that the finger spreads; (3) a broom-finish trowel stroke across wet concrete; (4) an excavator bucket that digs where you tap; (5) topsoil raked flat.
- A before/after slider as soon as there's a real driveway pair.
- A short "Driveway refresh vs new install" explainer if they say most calls are about that.
- Impeccable conflicts (kept on purpose): see the review notes below.

## Not verified
- Real-device touch, real SMS handoff on iOS/Android and inside Facebook's in-app browser, and whether the number receives texts at all.
- Frame rate on older phones (motion is CSS-only and light).
