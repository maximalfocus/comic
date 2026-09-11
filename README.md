# Comics

Four-panel comics made with `/comic`, posted in English to Substack and in Chinese to 小红书.

## Layout

```
YYYY/MM/<theme>/            one idea (theme), kebab-case English name
  README.md                 the shared thread, how en and zh differ, where each was published
  en/                       English version (Substack)
  zh/                       Chinese version (小红书)
```

Each language directory holds only the published final:

| File | What it is |
|---|---|
| `source.md` | the idea as given |
| `storyboard.md` | the approved storyboard |
| `prompts/01-page-<slug>.md` | the exact prompt that produced the final image |
| `01-page-<slug>.png` | the final comic |
| `substack-post.md` / `xiaohongshu.md` | the post text |

The two languages are created separately from the same thread, not translated: jokes, settings,
and characters are rebuilt for each audience, and only culture-neutral parts are shared.

## Version control

Tracked: everything above, including the final PNGs. Ignored: `render.sh` backups
(`*-backup-*.png`) and anything credential-like. Rejected candidates are not kept.
