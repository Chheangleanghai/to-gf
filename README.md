# 💗 For Her

A single self-contained page. No build step, no dependencies, no install.

## 1. Personalise it (10 minutes, and it's the whole ballgame)

Open `index.html` and find **`var CONFIG = {`** near the top of the `<script>` block.
That's the only place you need to touch.

| Key | What it does |
|---|---|
| `HER_NAME` | The greeting. `"Sarah"` → *"Sarah,"* |
| `YOUR_NAME` | The signature. `"Alex"` → *"— Always yours, Alex"* |
| `VOICE_SRC` | Your voice note. See §2. |
| `PHOTOS` | Photos behind the letter. See §3. |
| `DETAILS` | **The highest-impact edit on the page.** See below. |
| `REASONS` | The reasons jar. She pulls a different one every tap, forever. |

### `DETAILS` is the one that matters

This is what turns a pretty page into *your* page. Be tiny and specific:

- ❌ `"You are my everything."`
- ✅ `"I love that you narrate what the dog is thinking."`
- ✅ `"I still think about the time you fell asleep mid-sentence and denied it."`

Any line still starting with `TODO:` is **skipped silently** — so if you never get
round to it, nothing embarrassing ships. Fill them in anyway. It's the difference
between *"aww"* and actual tears.

## 2. Add your voice (do this one — it beats every animation on the page)

1. Record a voice note on your phone. 30–60 seconds. Read the letter, or just talk.
2. Name the file **exactly** `voice.mp3`.
3. Drop it next to `index.html`.

That's it. The player appears automatically, and it auto-starts when she taps the heart.

No file? The player never shows up. Nothing breaks.

## 3. Add photos (optional)

1. Drop images into the `photos/` folder.
2. Un-comment the matching lines in `CONFIG.PHOTOS`.

4–6 photos, portrait, under ~1 MB each. Missing photos are skipped silently.

## 4. Check it locally

Double-click `index.html`. It works straight off the filesystem.

## 5. Put it on a real link she can tap

### The easy way — Netlify Drop (no account, no install, ~2 min)

1. Add your photos and `voice.mp3` **first**.
2. Go to **https://app.netlify.com/drop**
3. Drag this whole folder onto the page.
4. You get a live URL immediately, e.g. `https://cheerful-panda-42.netlify.app`
5. **Text her that link.**

Optional: sign up (free) to keep the site permanently and rename it to something
like `https://for-her.netlify.app`.

> Make sure `index.html` is at the **top level** of the folder you drag — Netlify
> serves it as the homepage.

## Notes

- She will almost certainly open this on her **phone**. It's built mobile-first, but
  test it there yourself before sending.
- Respects `prefers-reduced-motion`, so it degrades gracefully for anyone sensitive
  to animation.
- Tapping anywhere throws hearts. That's intentional.
