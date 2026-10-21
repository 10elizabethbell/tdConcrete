---
name: TD Concrete
description: Calm band site for an Essex County excavating and concrete crew; phone-first quote requests.
colors:
  paper: "#f4f6fb"
  card: "#ffffff"
  field: "#e6ecf5"
  ink: "#12263a"
  body: "#2b3a4a"
  soft: "#4a5868"
  navy: "#1f3d5a"
  deep: "#102234"
  on-dark: "#f4f7fb"
  on-dark-soft: "#c9d6e4"
  amber: "#f2a93b"
  amber-2: "#f6bd62"
  amber-ink: "#8a5200"
  line: "rgba(18,38,58,.12)"
  focus: "#1f5fa8"
  error: "#b3261e"
typography:
  display:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(42px, 12vw, 80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-.005em"
  headline:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(30px, 7.6vw, 48px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-.005em"
  title:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(20px, 5.4vw, 24px)"
    fontWeight: 400
    lineHeight: 1.15
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 19px)"
    fontWeight: 400
    lineHeight: 1.55
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.2
rounded:
  field: "10px"
  card: "24px"
  pill: "999px"
spacing:
  gutter-phone: "20px"
  gutter-desk: "40px"
  band-phone: "64px"
  band-desk: "96px"
  stack: "16px"
  list-offset: "32px"
  container: "1160px"
components:
  button-primary:
    backgroundColor: "{colors.amber}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.amber-2}"
    textColor: "{colors.ink}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  service-row-arrow:
    backgroundColor: "rgba(255,255,255,.1)"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.pill}"
    size: "44px"
  service-row-arrow-hover:
    backgroundColor: "{colors.amber}"
    textColor: "{colors.ink}"
  photo-card:
    backgroundColor: "{colors.field}"
    textColor: "#ffffff"
    rounded: "{rounded.card}"
  form-card:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.card}"
    padding: "clamp(20px, 5vw, 32px)"
  input:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  chip:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "48px"
  chip-selected:
    backgroundColor: "{colors.ink}"
    textColor: "#ffffff"
  step-number:
    backgroundColor: "{colors.amber}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: "48px"
  float-circle:
    backgroundColor: "{colors.amber}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: "60px"
---

# Design System: TD Concrete

## Overview

**Creative North Star: "The Yard Crew's Flyer, Calmed Down"**

Ellie's calm band style (`~/.claude/skills/pitch-site/references/calm-photo-style.md`) applied to a trades outfit. The page is a stack of full-width colour bands: off-white paper, slate navy and deep navy with faint diagonal lines. One warm accent, machine amber, comes from the trade (excavators, safety gear). The client has no logo or colours, so the TD mark is a navy tile with an amber ground line. Density is low and type is large. Every interactive path ends at the phone number or the quote form.

Photos are **generated examples of each service, not the client's jobs.** The alt text starts with "Example:" and the cards carry no captions that claim otherwise. Swap them for real photos once the owner sends some (provenance is in `HANDOFF.md`).

**Key Characteristics:**
- Full-width bands that alternate paper, navy and deep navy. No boxed sections.
- Amber is used as a fill only. When it has to be text on a light ground, it darkens to amber-ink.
- Cal Sans at weight 400 for every heading, label, button and the big phone number. System sans for running text.
- Flat surfaces. The only shadow belongs to the floating text circle.
- Motion is limited to the hero H1 letter bounce-in and one 12px fade-up for content below the first screen.

## Colors

Cool slate neutrals with one warm machine-amber voice.

### Primary
- **Machine Amber** (#f2a93b): primary button fill, step numbers, the floating circle, the arrow on hover or focus, the `::selection` background, and the accent phrase on dark bands. The text on it is always ink.
- **Amber Lift** (#f6bd62): hover state of amber fills only.
- **Amber Ink** (#8a5200): amber's text and icon form on light grounds, used for the header phone icon, the care-list icons and the header phone hover.

### Neutral
- **Cool Paper** (#f4f6fb): page ground, header, photo and care bands, form band.
- **Card White** (#ffffff): the form card.
- **Field Mist** (#e6ecf5): inputs, unselected chips, the "sent" panel and the photo-card placeholder.
- **Slate Navy** (#1f3d5a): services and closing bands, and the TD mark tile.
- **Deep Navy** (#102234): hero overlay, how-it-works band and footer, always with the line texture.
- **Ink** (#12263a): headings on light grounds, text on amber, selected chips.
- **Body Slate** (#2b3a4a) / **Soft Slate** (#4a5868): running text and secondary text on light grounds.
- **On-Dark** (#f4f7fb) / **On-Dark Soft** (#c9d6e4): headings and body text on navy and deep navy.
- **Hairline** (rgba(18,38,58,.12)): dividers between care-list rows. On dark grounds the dividers use rgba(255,255,255,.14).
- **Focus Blue** (#1f5fa8) / **Error Red** (#b3261e): form hover and focus outline, and validation messages.

### Named Rules
**The Amber-Is-Fill Rule.** Amber (#f2a93b) never sets text on a light ground. On light grounds it becomes amber-ink (#8a5200). Text sitting on amber is ink (#12263a).

**The Dark-Band Accent Rule.** A heading's closing phrase goes amber (`.accent`) only on hero, navy or deep bands. Paper-band headings stay all ink.

**The Two-Focus Rule.** On light grounds focus is focus-blue (#1f5fa8), which keeps it distinct from the amber fills. On navy, deep, hero and footer grounds the focus outline switches to amber. The outline is 3px with a 3px offset.

## Typography

**Display Font:** Cal Sans (with Avenir Next, Segoe UI, system-ui)
**Body Font:** System sans (-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial)

**Character:** A rounded, friendly display face at a single weight (400) does all the shouting. The plain system body keeps the page fast and native on phones.

### Hierarchy
- **Display** (400, clamp(42px,12vw,80px), 1.02, max 12ch): the hero H1 only, in white.
- **Headline** (400, clamp(30px,7.6vw,48px), 1.08, `text-wrap:balance`): one H2 per band.
- **Title** (400, clamp(20px,5.4vw,24px), 1.15): service rows and care-list items. Photo-card titles step up to clamp(22px,6vw,26px), and step titles are 21px (22px at 1024px and up).
- **Lede** (system, clamp(17px,4.6vw,19px), 1.55, max 38ch): the line under a band heading, in soft slate. The hero promise is clamp(17px,4.7vw,20px).
- **Body** (system, 16px, 1.7): running text. Inputs are 16px so iOS does not zoom.
- **Label** (Cal Sans 400, 17px, 1.2): form labels and legends. Buttons use 18px and the header phone 17px (20px on desktop). Small helper text is 14px system.
- **Big phone** (Cal Sans, clamp(30px,9vw,52px)): the closing band's phone number, with an amber phone icon at 0.8em.

### Named Rules
**The One-Weight Display Rule.** Cal Sans is only ever set at weight 400. Hierarchy comes from size alone, never from bold.

## Layout

The container is 1160px wide with a 20px gutter, widening to 40px at 760px and up. Bands are padded 64px top and bottom, 96px at 760px and up. A band that follows another band of the same colour drops its top padding (the care band after the photo band) so the two read as one surface. Content stacks with 16px gaps in heads and a 32px offset before lists.

Breakpoints: **760px** (hero becomes a side-lit full-bleed photo, services go to two columns, photo cards to three columns at 4:5) and **1024px** (care and form go to a two-column split with a 64px gap, the form head becomes sticky, steps go to three columns, the closing band puts heading and big phone side by side). There is also a landscape-phone rule (760px+ and max-height 520px) that shrinks the hero so its buttons stay on the first screen.

**Hero.** On phones the copy sits on solid deep navy and the photo shows as a strip below the buttons. Its height is set by `--peek`, clamp(230px,62vw,300px), and a gradient fades from the navy into the photo. On desktop a left-to-right deep-navy gradient covers the full-bleed photo (.94 to .15 opacity).

## Elevation & Depth

The system is flat. Depth comes from the colour of each band and from the deep-navy line texture (`repeating-linear-gradient(135deg, transparent 0 22px, rgba(255,255,255,.035) 22px 23px)`). Photo cards have a bottom scrim (deep navy, 0 to .85 opacity from 45% down) so their titles stay legible.

### Shadow Vocabulary
- **Float lift** (`box-shadow: 0 10px 28px rgba(8,22,36,.3)`): the floating text circle only.

### Named Rules
**The One-Shadow Rule.** Nothing rests on a shadow except the fixed floating circle, because it is the only thing that sits above the page.

**The Texture-Means-Deep Rule.** The line texture appears on deep navy grounds only: hero, how-it-works and footer. It never appears on slate navy or paper.

## Shapes

There are three radii. Pills (999px) for buttons, chips and link-buttons. Gently curved cards (24px) for photo cards and the form card. Soft fields (10px) for inputs. Circles are used for the arrow (44px), step numbers (48px) and the float (60px). There are no borders on surfaces. Only list rows carry 1px hairlines, top and bottom.

## Components

### Buttons
- **Shape:** pill (999px), at least 56px tall, padded 0 26px, Cal Sans 18px, 2px border.
- **Primary:** amber fill with ink text. Hover goes to amber-2. Active scales to 0.98. Inside the form the button is full width and its hover adds a 2px focus-blue outline.
- **Ghost:** transparent with on-dark text and a 70%-white border. Used on the hero only. Hover gives a white border and a 10% white fill.
- **Link-button** (inside the form's fallback panel): 44px pill with a 2px ink outline. Hover turns it focus-blue.
- In the hero, buttons stack full width on phones. From 760px they sit in a row at a minimum width of 220px.

### Service rows (signature)
- Each row is a whole link, at least 72px tall, in title type on slate navy, with a 1px rgba(255,255,255,.14) hairline between rows. Every row links to `#quote` and preselects the matching job chip through `data-job`.
- **Arrow-only hover:** the row itself never changes (no background, no shadow, no outline). Only its 44px circle arrow changes, from a 10% white fill to amber with ink. Keyboard focus does the same to the arrow and adds an amber outline.

### Photo cards
- 24px-radius links: 4:3 on phones, 4:5 in three columns from 760px. Each has a field-mist placeholder, a bottom scrim, a white title at the bottom left and a solid amber arrow (amber-2 on hover). They also preselect the job chip.
- Images are generated examples with "Example:" alt text and no captions.

### Care list
- Rows in title type and ink, each with a 40px line icon in amber-ink (stroke 2.4), separated by hairlines. A second, `hidden` list holds the owner's unverified claims ("35+ years", "Fully insured", "Locally owned"). Unhide it only once the owner confirms them.

### Steps
- An ordered list on deep navy. Each step has a 48px amber circle with a CSS counter number in Cal Sans 20px, a Cal Sans title and a plain line underneath. One column on phones, three columns at 1024px.

### Quote form
- A white card (24px radius) with 20px gaps. Job choice is a radio row of chips: 48px field-mist pills, ink fill with white text when selected, focus-blue border on hover or focus.
- Inputs are field-mist with a 10px radius and a 2px transparent border that turns focus-blue on hover or focus. Errors give a red border and a red message below.
- Submitting composes an SMS to `CONFIG.SMS`. If no messages app opens, a fallback panel appears after 900ms with the message text, a "Copy message" button and an "Open in Messages" link. Picking a job changes the textarea placeholder to a job-specific prompt.

### Closing band
- Slate navy. The heading has an amber accent phrase, followed by a soft "who" line, a service-area line and the big phone number. At 1024px and up the text and the number sit in a two-column grid, aligned to the bottom.

### Floating text circle
- A single 60px amber circle with a chat icon, fixed at the bottom right inside the safe area. It links to `sms:` with a prefilled greeting. It slides in from 120px below (350ms, cubic-bezier(.2,.8,.2,1)) once the hero leaves the screen and hides while the form is on screen. When hidden it gets `tabindex=-1` and `aria-hidden`. It is never a bottom bar.

### Header
- Paper. On the left, the TD mark (36px, hidden under 375px) with the Cal Sans wordmark and an 11px uppercase tracked descriptor. On the right, a tap-to-call number with an amber-ink phone icon. Both targets are at least 44px.

### Motion
- **Hero H1 bounce-in:** JS splits the heading into letters. Each letter slides in from translateX(50px), 1s on cubic-bezier(.34,1.56,.64,1), staggered 20ms. Once the last letter lands, the plain heading markup is restored so kerning and text selection come back. The aria-label holds the full text while the split is in place.
- **Fade-up:** elements marked `.rise` that start below the first screen fade in, opacity 0 to 1 and translateY(12px) to 0, over 400ms ease-out, triggered when they enter the viewport.
- **Reduced motion:** no letter split, no fade-up, no transitions on buttons, arrows or the float, and auto scroll-behavior.
- **No JS:** the heading stays plain. Everything is visible at rest, because the hidden state only applies under `html.js`. The float is removed if IntersectionObserver is missing.

### CONFIG switches (top of the script)
- `SMS` (`'+15197967967'`): the number for texts. The owner has not yet confirmed it takes texts.
- `NAME` (`'TD Concrete'`): the name used in the composed message.
- `TEXTS` (`true`): set to `false` if the number can't take texts. The float is removed, the submit button becomes "Call 519-796-7967" and dials instead, and the "Opens your messages" note is hidden.
- `FLOAT` (`true`): set to `false` to remove the floating circle.

## Do's and Don'ts

### Do:
- **Do** keep amber as a fill with ink text on it, and use amber-ink (#8a5200) when amber has to be text on paper.
- **Do** build new sections as full-width bands from the paper, slate navy and deep-navy-with-texture set, with 64/96px padding.
- **Do** make list-like actions whole-row links, with hover limited to the arrow circle.
- **Do** keep every tap target at least 44px (buttons 56px, chips 48px).
- **Do** label generated photos as examples in their alt text until the owner sends real job photos.
- **Do** keep content visible at rest. Motion may only hide what starts below the first screen, and only when JS is running and reduced motion is off.

### Don't:
- **Don't** add hover backgrounds, shadows or outlines to service rows.
- **Don't** put shadows on cards, buttons or bands. The float is the only lifted element.
- **Don't** set Cal Sans in bold, or headings in the system face.
- **Don't** replace the floating circle with a sticky bottom bar.
- **Don't** publish the hidden unverified claims, or present the generated photos as the crew's own work.
