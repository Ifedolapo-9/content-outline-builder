---
name: content-outline-builder
description: Build a publish-ready content outline for a blog post or article, or audit an existing outline for missing components. Produces the full brief a writer needs before drafting, covering the header block with keyword, intent, word count and ICP, plus competitor gap analysis, per-section directional guidance, key points, target keywords and internal links, an FAQ plan, and a flagged list of editorial dependencies. Use this whenever the user asks for an article outline, a content brief, a blog structure or a plan for a piece, when they hand over a keyword or SEO brief to turn into a structure, when they ask whether an outline is complete or what it is missing, or when they mention a content refresh, an outline review, or preparing an article for drafting. Trigger it even if they only ask for "a quick structure," since outlines that skip intent, ICP or competitor analysis fail at the draft stage.
---

# Content outline builder

Two jobs: **build** an outline from scratch, or **audit** one that already exists and fill the gaps.

A good outline is not a table of contents. It is the document that lets someone else draft the piece without guessing, and lets a reviewer disagree with the strategy before anyone writes 3,000 words. That means every section carries direction, not just a heading.

## Which mode

**Build** when the user has a topic, keyword, SEO brief, or refresh target and no outline yet.

**Audit** when an outline exists. Check it against the required components below, report what is missing or thin, then supply the missing parts. Do not rewrite what is already good.

If the user hands over a partial outline, that is an audit that ends in a build.

## Before you start

Gather what exists, and say in the output which checks were done blind:

- **The brief or keyword data.** Primary keyword, secondary keywords, volumes, current rankings if it is a refresh.
- **The house style guide.** If one is in the project or conversation, it overrides anything here. Look for rules on dashes, spelling variant, heading case, paragraph length, and banned words.
- **The current URL**, if this is a refresh. Fetch it. You cannot mark sections Keep, Rework or Remove without reading what is there.
- **Competitor URLs.** The brief may list them. If not, search the primary keyword and take the top three.

Ask before starting only if genuinely blocked: whether it is a new piece or a refresh, and the target word count if no brief supplies one. Otherwise infer and state your assumption.

## Required components

An outline is incomplete without all of these. In audit mode, this is the checklist.

**Header block**
- Primary keyword
- Secondary and supporting keywords
- URL or slug
- Meta title
- Meta description, 150 to 155 characters, character count stated
- Search intent, named as a type: informational, commercial investigation, transactional, navigational
- Word count target
- ICP, derived through the empathy map, see `references/empathy-map.md`

**Strategy block**
- Competitor gap analysis, two to three competitors, what to match and what to exploit, see `references/writing-the-outline.md`
- The angle, stated as a claim someone could disagree with
- Structural decisions with rationale, so a reviewer can object before drafting

**Per section**
- Heading, with level marked, H2 or H3
- Action label, for refreshes: New, Keep, Keep and tighten, Rework, Remove
- Directional guidance, what to do, not what the section is about
- Key points to cover, as bullets
- Target keywords for that section
- Internal links, placed in the section where the reader needs them

**Closing**
- FAQ plan, questions with a one-line steer each, plus a note on schema
- Related articles
- Editorial dependencies, the things that must be resolved before or during drafting

Word budget per section is optional. Include it unless the user has said they do not want it.

## Build workflow

1. **Read the brief and the current page.** For a refresh, fetch the live URL and note what each existing section does.
2. **Search the SERP.** Read the top three results properly. Note what format ranks, what depth, what every one of them covers, and what none of them covers. That last gap is the outline's reason to exist.
3. **Derive the ICP** through the empathy map. Always. See `references/empathy-map.md`.
4. **Write the strategy block first.** The angle and the structural decisions determine every section below them. If you cannot state an angle someone could argue with, you do not have a piece yet.
5. **Build the sections**, using `references/outline-template.md` for shape and `references/writing-the-outline.md` for how to write the guidance.
6. **Flag dependencies.** Dead internal links, contradictory pricing, stale figures, promo codes, missing test data, anything that will block the writer.
7. **Deliver as a file**, in the house brief format if one exists.

## Audit workflow

1. Read the outline in full.
2. Check it against the required components list.
3. Report in three tiers: **Missing**, blocking; **Thin**, present but not actionable; **Present**.
4. Supply the missing components. For thin ones, show what the upgraded version looks like rather than describing it.
5. Do not restructure a sound outline to match a preferred shape. Fix what is absent.

## The quality bar

The test for any line in an outline: **could the writer act on this without asking a question?**

"Discuss pricing" fails. "Open with a 40 to 80 word definition written to stand alone as a quotable answer, then the pricing table, sourced from each vendor's page on the day of publication and date-stamped" passes.

Three habits separate a usable outline from a decorative one:

**Direction over description.** Tell the writer what to do with the section, not what it contains.

**Rationale where the decision is contestable.** If a section is being cut, moved or reframed, say why in one line. That is what lets a reviewer object early instead of at draft stage.

**Links in place.** An internal link named inside the section that needs it gets used. A list of links at the bottom gets dumped into a footer.

## Special cases

**Comparison and "tested" articles.** The outline must specify the test before drafting: targets, criteria, exclusions, how many runs, what counts as a correct result, and how ownership is disclosed if the publisher is in the comparison. An outline that says "test the tools" produces an article that fails review.

**Refreshes.** Every existing section gets an action label. Cannibalisation check across the site's other URLs for the same term. Note which existing links live in sections being cut, because they need rehoming.

**Product-led content.** State where the product mention goes and why it is earned there. Concessions and honest limitations come before the pitch, never after.

## Output

One file, in the user's house format if one exists, otherwise the template in `references/outline-template.md`.

Then summarise in chat: the angle in one line, the two or three structural calls worth arguing about, and anything you had to assume. Lead with the strategy, not the section list.

## Reference files

- `references/outline-template.md`, the fill-in template with annotations
- `references/empathy-map.md`, the ICP derivation process
- `references/writing-the-outline.md`, competitor analysis, action labels, directional guidance, common failures
