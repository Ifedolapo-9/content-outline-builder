# Content Outline Builder

A Claude skill that builds publish-ready content outlines for blog posts and articles. It can also audit an outline you already have and fill in what's missing.

A good outline is not a table of contents. It's the document that lets someone else draft the piece without guessing, and lets a reviewer push back on the strategy before anyone writes 3,000 words. This skill holds every outline to that standard.

---

## What it does

The skill works in two modes:

- **Build:** give it a topic, a keyword, an SEO brief, or a page to refresh. It reads the search results, works out who the reader is, finds the gaps your competitors leave open, and writes a full outline with direction for every section.
- **Audit:** give it an existing outline. It checks the outline against a fixed list of required components, sorts the results into **Missing**, **Thin** and **Present**, and then writes the missing parts. It leaves the sections that already work alone.

If you hand it a partial outline, it runs an audit first and then builds the rest.

You get one outline file plus a short summary in chat. The summary covers the angle, the structural calls worth arguing about, and any assumptions the skill had to make.

## Who it's for

- **Content writers and technical writers** who want a brief they can draft from without going back to ask questions
- **Content strategists and SEO leads** who write briefs for other people to draft
- **Editors** who review outlines and want to catch strategy problems before the draft stage
- **Freelancers and agencies** who refresh client content and need to decide what to keep, rework or cut

## Key benefits

- **Direction, not description.** Every section tells the writer what to do. "Discuss pricing" becomes "Open with a 40 to 80 word definition that stands alone as a quotable answer, then the pricing table, sourced from each vendor's page on the day of publication."
- **An ICP built from evidence.** The audience comes from an empathy map filled in from the keyword set, the search results and competitor pages, not from a job title someone guessed.
- **Competitor gaps you can defend.** It names what to match and what to exploit for two to three competitors, and explains why each gap exists. For example, a vendor can't recommend against its own product, so that's a gap you can take.
- **A stated angle.** The outline commits to a claim someone could disagree with. If there's no angle, there's no piece yet.
- **Early pushback.** Structural decisions come with a one-line rationale, so a reviewer can object at the outline stage instead of after the draft.
- **Clear refresh decisions.** On a content refresh, every existing section gets an action label, and the skill flags internal links that sit inside sections being cut.
- **Fewer blockers mid-draft.** Dead links, conflicting pricing, stale figures and missing test data are listed before drafting starts.

## Components

An outline isn't complete without all of these. In audit mode, this is the checklist.

### Header block

- Primary keyword
- Secondary and supporting keywords
- URL or slug
- Meta title
- Meta description, 150 to 155 characters, with the character count stated
- Search intent, named as a type: informational, commercial investigation, transactional or navigational
- Word count target
- ICP, derived through the empathy map (see [`references/empathy-map.md`](skills/content-outline-builder/references/empathy-map.md))

### Strategy block

- Competitor gap analysis covering two to three competitors, with what to match and what to exploit (see [`references/writing-the-outline.md`](skills/content-outline-builder/references/writing-the-outline.md))
- The angle, stated as a claim someone could disagree with
- Structural decisions with their rationale, so a reviewer can object before drafting

### Per section

- Heading, with the level marked (H2 or H3)
- Action label for refreshes: New, Keep, Keep and tighten, Rework or Remove
- Directional guidance: what to do in the section, not what it's about
- Key points to cover, as bullets
- Target keywords for that section
- Internal links, placed in the section where the reader needs them
- Word budget (optional, included by default)

### Closing

- FAQ plan: the questions, a one-line steer for each, and a note on schema
- Related articles
- Editorial dependencies: anything that has to be resolved before or during drafting

### Special cases it handles

- **Comparison and "tested" articles:** the outline defines the test before drafting, including targets, criteria, exclusions, number of runs, what counts as a correct result, and how ownership is disclosed if the publisher is in the comparison.
- **Refreshes:** every section gets an action label, the skill checks for cannibalisation across the site, and it flags links that need a new home.
- **Product-led content:** the outline says where the product mention goes and why it belongs there. Concessions and honest limitations come before the pitch.

## What's in the repo

```
content-outline-builder/
├── README.md
├── LICENSE
└── skills/
    └── content-outline-builder/
        ├── SKILL.md                        # Main instructions: modes, components, workflows
        └── references/
            ├── outline-template.md         # The fill-in template, with notes on each slot
            ├── empathy-map.md              # How to derive the ICP
            └── writing-the-outline.md      # Competitor analysis, action labels, directional guidance, common failures
```

## How to use it

### 1. Install

**Claude Code:** copy the skill folder into your skills directory.

```bash
git clone https://github.com/Ifedolapo-9/content-outline-builder.git

# Available in every project
cp -r content-outline-builder/skills/content-outline-builder ~/.claude/skills/

# Or only in one project
cp -r content-outline-builder/skills/content-outline-builder your-project/.claude/skills/
```

Restart Claude Code. The skill loads on its own when your request matches it.

**Claude.ai:** zip the `skills/content-outline-builder` folder, then upload it under **Settings → Capabilities → Skills**.

### 2. Ask for an outline

You don't need to name the skill. Describe what you want:

**Build a new outline**

> Build an outline for the keyword "web scraping with python". Target around 2,500 words. Competitors: [url1], [url2], [url3].

**Refresh an existing page**

> This is a content refresh for https://example.com/blog/rotating-proxies. Here's the SEO brief: [paste]. Outline the updated version.

**Audit an outline**

> Here's my outline for an article on API rate limiting. What's missing before it goes to the writer? [paste or attach]

**Ask for a quick structure**

> Give me a quick structure for a post comparing headless browsers.

Even for a quick structure, the skill still covers intent, ICP and competitors, because outlines that skip those tend to fail at the draft stage.

### 3. Give it more to work with

The skill makes reasonable assumptions and tells you what they were, but the output is better when you supply:

- **Keyword data:** primary and secondary keywords, volumes, and current rankings for a refresh
- **Your house style guide:** this overrides the skill's defaults on dashes, spelling, heading case and banned words
- **The live URL** for a refresh, so it can read what's there before labelling sections
- **Competitor URLs:** if you leave these out, it searches the primary keyword and uses the top three results

### 4. Review the summary first

Start with the summary in chat, before the section list. It tells you the angle and the structural calls worth arguing about. If you disagree with the strategy, now is the cheapest time to say so.

## Questions or ideas?

If you have a question about this skill, feedback on how it worked for you, or an idea for a new skill, message me on LinkedIn:

**[Ifedolapo Ojo on LinkedIn](https://www.linkedin.com/in/ifedolapo-ojo)**

Issues and pull requests on this repo are welcome too.

## License

[MIT](LICENSE)
