# Next Steps

## Completed
- New git repo created
- Git author confirmed as Koutian Wu <ktwu01@gmail.com>
- Research dossier created
- Milestone table v1 and v2 created
- Initial timeline / storymap JSON scaffold created
- First landing page prototype created
- SOTA design review added at `research/sota-design-review.md`
- Editorial content schema added:
  - `data/chapters.json`
  - `data/locations.json`
  - `data/validation.json`
  - `data/sources.json`
  - `data/artifacts.json`
- Landing page rebuilt into an editorial chronicle with:
  - premium hero + thesis framing
  - phase rail / quick navigation
  - narrative timeline chapters
  - synced MapLibre geography module
  - curated validation groups
  - denser reference timeline sourced from `data/timeline.json`
  - source archive
  - source-backed editorial artifact cards for the strongest chapters

## Next implementation steps
1. Strengthen the source archive further by capturing more direct primary URLs for early academic/founding details.
2. Add a lightweight artifact/media taxonomy so chapters can distinguish article snippets, announcements, conference appearances, and future image assets.
3. Refine the map chapter experience with tighter camera presets and subtle chapter-to-route emphasis instead of a single global route treatment.
4. Introduce a stronger chapter-end CTA / present-direction module so the chronicle lands on why Sean Xiang matters now.
5. Consider migrating the static prototype into Astro once the content model stabilizes.
