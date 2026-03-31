# Images Directory

## How to Add Images to OBSKIRA RUNWAY

### Image Placeholders

The investor brief currently has **3 image placeholders** waiting to be filled (in Section II):
- **Piece 1** — Product photo location (line 332 in index.html)
- **Piece 2** — Product photo location (line 336 in index.html)
- **Piece 3** — Product photo location (line 340 in index.html)

### Steps to Add Images

1. **Save optimized images** to this `images/` folder:
   - Use `.jpg` or `.png` format
   - Optimize file size to **300–500 KB** per image
   - Recommended dimensions: **450px × 600px** (3:4 aspect ratio)
   - Filenames: `piece-1.jpg`, `piece-2.jpg`, `piece-3.jpg`

2. **Edit index.html** to replace placeholders with `<img>` tags:

   **Find this (around line 330):**
   ```html
   <div class="img-grid">
     <div class="img-box">[ Insert photo — Piece 1 ]</div>
     <div class="img-box">[ Insert photo — Piece 2 ]</div>
     <div class="img-box">[ Insert photo — Piece 3 ]</div>
   </div>
   ```

   **Replace with:**
   ```html
   <div class="img-grid">
     <div><img src="images/piece-1.jpg" alt="OBSKIRA Piece 1" style="width:100%; aspect-ratio:3/4; object-fit:cover;"><p class="img-caption">Design I</p></div>
     <div><img src="images/piece-2.jpg" alt="OBSKIRA Piece 2" style="width:100%; aspect-ratio:3/4; object-fit:cover;"><p class="img-caption">Design II</p></div>
     <div><img src="images/piece-3.jpg" alt="OBSKIRA Piece 3" style="width:100%; aspect-ratio:3/4; object-fit:cover;"><p class="img-caption">Design III</p></div>
   </div>
   ```

3. **Add captions** (optional):
   - Update "Design I", "Design II", "Design III" to match piece names
   - Captions appear below each image

4. **Test locally**:
   ```bash
   npm run dev
   ```
   Visit `http://localhost:8000` to see images render

5. **Commit and push**:
   ```bash
   git add .
   git commit -m "Add product photos to Section II"
   git push origin main
   ```

### Image Guidelines

- **Quality**: High-resolution product shots (minimum 450px wide)
- **Format**: JPG for photos, PNG for graphics with transparency
- **Styling**: Images automatically adapt to mobile (1 column on screens <600px)
- **Alt Text**: Always include descriptive alt text for accessibility
- **Mobile**: Images scale responsively without manual responsive breakpoints

### Environment Variables

Images are served from the root directory with relative paths. No server configuration needed.

### Troubleshooting

**Images not showing after push?**
- Wait 1–2 minutes for Vercel/Netlify to finish deployment
- Clear browser cache (Cmd+Shift+Delete)
- Verify relative paths use `images/filename.jpg` (no leading `/`)

**Image looks distorted?**
- Check aspect ratio (3:4 is ideal)
- Use `object-fit: cover` in the `<img>` style to preserve ratio

**File size too large?**
- Compress JPGs to 300–500 KB using:
  - macOS: Preview → Tools → Adjust Size
  - Online: TinyJPG.com or Squoosh.app
  - CLI: `sips -Z 450 piece-1.jpg`
