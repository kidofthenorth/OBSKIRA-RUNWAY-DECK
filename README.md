# OBSKIRA RUNWAY — Investor Brief

A luxury fashion brand investor presentation deck. Clean, minimal design with smooth animations and responsive layout.

## Features

- 📱 **Fully Responsive** — Optimized for mobile, tablet, and desktop
- ✨ **Smooth Animations** — Elegant fade-in effects on sections
- 🎨 **Premium Design** — Custom typography with Playfair Display and Inter fonts
- 🔄 **Static HTML** — No build process required, deploy anywhere
- ⚡ **Fast Loading** — Lightweight CSS-only animations

## Project Structure

```
obskira-runway-deck/
├── index.html          # Main presentation file
├── package.json        # Project metadata
├── vercel.json         # Vercel deployment config
├── .gitignore          # Git ignore rules
├── README.md           # This file
└── .github/
    └── copilot-instructions.md
```

## Local Development

### Prerequisites
- Node.js 14+ (optional, for local server)
- Any modern web browser

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/obskira-runway-deck.git
   cd obskira-runway-deck
   ```

2. **Install dependencies** (optional)
   ```bash
   npm install
   ```

3. **Start local server**
   ```bash
   npm run dev
   ```
   Server runs at `http://localhost:8000`

4. **Open in browser**
   - Simply open `index.html` in your browser, or
   - Use the local server URL above

## Deployment

### Option 1: Deploy to Vercel (Recommended)

1. **Sign up at Vercel**
   - Go to [vercel.com](https://vercel.com) and create an account

2. **Connect your GitHub repository**
   - Click "New Project" → "Import Git Repository"
   - Select your OBSKIRA repository
   - Vercel auto-detects it as a static site

3. **Deploy**
   - Click "Deploy"
   - Your site is live! Visit your Vercel dashboard for the URL

4. **Auto-deploy**
   - Every push to `main` branch auto-deploys
   - View deployments in Vercel dashboard

### Option 2: Deploy to GitHub Pages

1. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Source: Select `main` branch
   - Save

2. **Your site is live**
   - URL: `https://yourusername.github.io/obskira-runway-deck`
   - Updates automatically on each `main` branch push

### Option 3: Deploy to Netlify

1. **Sign up at Netlify**
   - Go to [netlify.com](https://netlify.com)

2. **Connect repository**
   - Click "New site from Git"
   - Select GitHub & authorize
   - Choose your repository

3. **Deploy settings**
   - Build command: (leave blank)
   - Publish directory: `.`
   - Click "Deploy site"

## Setting Up GitHub Repository

### First Time Setup

1. **Initialize local git** (if not already done)
   ```bash
   git init
   git add .
   git commit -m "Initial commit: OBSKIRA RUNWAY investor brief"
   ```

2. **Create repository on GitHub**
   - Go to [github.com/new](https://github.com/new)
   - Name: `obskira-runway-deck`
   - Description: "OBSKIRA RUNWAY — Investor Brief"
   - Choose Private or Public
   - **Do NOT** initialize with README, .gitignore, or license
   - Click "Create repository"

3. **Add remote & push**
   ```bash
   git remote add origin https://github.com/yourusername/obskira-runway-deck.git
   git branch -M main
   git push -u origin main
   ```

### Future Updates

```bash
# Make changes, then:
git add .
git commit -m "Your changes here"
git push origin main
```

## Customization

### Edit Content
- Open `index.html` in any text editor
- Modify text, numbers, or sections directly
- Save and refresh browser to see changes

### Add Images
- Create an `images/` folder
- Add your fashion photography
- Update the placeholder divs:
  ```html
  <div class="img-box">[ Insert photo — Piece 1 ]</div>
  ```
  Replace with:
  ```html
  <img src="images/piece-1.jpg" alt="Piece 1">
  ```

### Update Styling
- All CSS is in the `<style>` block in `index.html`
- Colors: `#8b0000` (wine red), `#e8e8e3` (off-white), `#0a0a0a` (dark)
- Modify font sizes, spacing, or animations as needed

### Change Domain
- **Vercel**: Go to Vercel dashboard → Settings → Domains → Add custom domain
- **GitHub Pages**: Go to Settings → Pages → Custom domain
- **Netlify**: Go to Site settings → Domain management → Add custom domain

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Android)

## Performance Tips

- Images: Optimize before deployment (compress, modern formats like WebP)
- Use CDN: Vercel & Netlify provide global CDN by default
- Analytics: Add Google Analytics or Vercel Analytics without affecting performance

## Troubleshooting

### Site not updating after push?
- Clear browser cache (Cmd+Shift+Delete)
- Wait 1-2 minutes for deployment to complete
- Check deployment status in Vercel/Netlify dashboard

### Local server won't start?
```bash
# Kill existing process on port 8000
lsof -ti:8000 | xargs kill -9
npm run dev
```

### Images not loading?
- Check file paths are relative: `images/photo.jpg` not `/images/photo.jpg`
- Ensure image files exist in the same directory structure
- Images must be committed to git

## License

Confidential — OBSKIRA RUNWAY

## Contact & Support

For questions or updates to the investor brief, contact the team directly.

---

**Last Updated:** March 2026  
**Hosted on:** [Vercel](https://vercel.com) | [GitHub](https://github.com)
