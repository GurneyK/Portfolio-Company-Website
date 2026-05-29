# H3L Showreel Studio

This repo contains a SharePoint-friendly interactive video portfolio for the H3L team.

## Files

- `index.html` is the normal browser/GitHub Pages version.
- `h3l-project-reel-library.aspx` is the same page mirrored for SharePoint testing.
- `h3l-showreel-pink.html` is an alternate H3L-color version with a stronger royal blue, violet, cyan, and pink palette.
- `h3l-showreel-pink.aspx` is the matching active-page version of the alternate color treatment.
- `h3l-showreel-blue.html` is a brighter H3L version with a blue and white base plus small pink and purple accents.
- `h3l-showreel-blue.aspx` is the matching active-page version of the blue color treatment.
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

## Adding Another Project

1. Add the MP4 to `assets/videos/`.
2. Add a poster image to `assets/posters/`.
3. Open `index.html` and copy one object inside the `PROJECTS` array near the bottom.
4. Update the copied object's `id`, `title`, `category`, `video`, `poster`, `runtime`, `seconds`, `purpose`, `people`, `outcome`, `tags`, `description`, and `chapters`.
5. Copy the updated `index.html` content into `h3l-project-reel-library.aspx`.

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

## SharePoint Note

SharePoint Online may block custom `.aspx` files unless custom script is enabled for the site and the uploader has the right permissions. If the `.aspx` downloads instead of rendering, ask the SharePoint admin whether custom script is allowed for that specific site.
