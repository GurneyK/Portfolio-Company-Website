# H3L Showreel Studio

This repo contains the H3L interactive video portfolio for company website hosting.

## Files

- `index.html` is the main page your IT team should host.
- `assets/videos/` stores project trailer videos.
- `assets/posters/` stores poster images used by cards and the hero.
- `assets/brand/` stores the H3L logo.

## Experience Features

- Cinematic hero with animated canvas texture and a live project preview.
- Sticky navigation with a skip link for keyboard users.
- Search and category filters for the project gallery.
- Featured project dock for fast switching between trailers.
- Focused video player with details, tags, outcomes, and team credits.
- Cinema mode for a larger viewing experience.
- Copyable project links using each project's `id` hash.
- Dynamic story map that explains what to notice while watching.
- Per-project comments that appear under the active video and roll up into the reactions wall.

## Owner-Only Project Updates

The live page does not include public video uploads. New trailers should be added only by the page owner or approved repo maintainer.

1. Add the MP4 to `assets/videos/`.
2. Add a poster image to `assets/posters/`.
3. Open `index.html` and copy one object inside the `PROJECTS` array near the bottom.
4. Update the copied object's `id`, `title`, `category`, `video`, `poster`, `runtime`, `seconds`, `purpose`, `people`, `outcome`, `tags`, `description`, and `chapters`.

## Comments

Comments work immediately in browser storage for previewing and demos. For shared live comments across all viewers, connect a team endpoint in `COMMENT_SETTINGS.endpoint` near the `PROJECTS` block. The page posts this JSON shape:

```json
{
  "id": "generated-id",
  "projectId": "design-library",
  "projectTitle": "Design Library",
  "name": "Reviewer name",
  "team": "Team or role",
  "text": "Comment text",
  "createdAt": "2026-05-27T00:00:00.000Z"
}
```

## Hosting Note

Host `index.html` from the repo root and keep the `assets/` folder beside it so video and poster paths resolve correctly.
