# Space Doodles Reel

A simple pipeline that automatically stitches Space Doodles clips into a single seamless reel.

Upload short video clips and they will automatically be merged into one continuous video and deployed to the site.

---

## How it Works

1. Upload a `.mp4` clip to:

```
/public/videos
```

2. GitHub Actions automatically runs.

3. `ffmpeg` merges all clips into:

```
/public/reel.mp4
```

4. Vercel redeploys the site.

5. The updated reel plays on the webpage.

---

## Project Structure

```
public/
  videos/        # Individual clips
  reel.mp4       # Auto-generated stitched reel
  index.html     # Simple player page

.github/workflows/
  build-reel.yml # GitHub Action that builds the reel
```

---

## How to Add a Clip

Upload a `.mp4` file to:

```
public/videos/
```

Example filenames:

```
2215.mp4
5421.mp4
9481.mp4
```

The workflow will automatically rebuild the reel.

---


## Tech Used

- GitHub Actions
- FFmpeg
- Vercel static hosting
- Simple HTML5 video player

---

## Why This Exists

Space Doodles clips are short and loopable.  
When stitched together they create a continuous audiovisual chain.

This repo provides a lightweight way for a community to build a shared reel.

---

## License

MIT
