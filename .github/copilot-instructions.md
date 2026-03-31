<!-- Use this file to provide workspace-specific custom instructions to Copilot. For more details, visit https://code.visualstudio.com/docs/copilot/copilot-customization#_use-a-githubcopilotinstructionsmd-file -->

# OBSKIRA RUNWAY — Project Guidelines

## Project Overview
- **Name:** OBSKIRA RUNWAY — Investor Brief
- **Type:** Static HTML/CSS web application
- **Framework:** None (vanilla HTML5 + CSS3)
- **Deployment:** Vercel, GitHub Pages, or Netlify
- **Main File:** `index.html`

## Key Files & Purpose
- `index.html` — Complete investor presentation in a single HTML file
- `package.json` — Project metadata and dev scripts
- `vercel.json` — Vercel deployment configuration
- `.gitignore` — Git ignore rules
- `README.md` — Comprehensive deployment and customization guide

## Development Workflow

### Local Development
```bash
npm install          # Install dependencies (optional)
npm run dev          # Start local server on port 8000
```

### Making Changes
1. Edit `index.html` directly for content updates
2. CSS is embedded in the `<style>` block — modify there for styling
3. Save file and refresh browser
4. Test responsive design across breakpoints

### Committing Changes
```bash
git add .
git commit -m "Descriptive message"
git push origin main
```

## Customization Guidelines

### Content Updates
- **Text:** Edit directly in HTML sections
- **Colors:** Primary wine color is `#8b0000`, text is `#e8e8e3`, background is `#0a0a0a`
- **Typography:** Uses Playfair Display (serif headings) and Inter (body text)
- **Numbers/Stats:** Update table values and stat blocks as needed

### Adding Images
- Create `images/` folder in project root
- Include optimized JPG/PNG files
- Reference with relative paths: `<img src="images/filename.jpg">`
- Update placeholder divs (search for `[ Insert photo` comments)

### Styling
- All CSS is in `<style>` block
- Mobile breakpoint: `max-width: 600px`
- Smooth animations pre-built (fade-in effects)
- No external CSS files needed

### Responsive Design
- Mobile-first approach
- Grid layouts adapt from 3 columns to 1 column on mobile
- Font sizes use `clamp()` for fluid scaling
- Padding and margins adjust automatically

## GitHub & Deployment Setup

### GitHub Initialization (One-time)
1. Create repo on github.com/new
2. Name: `obskira-runway-deck`
3. Run locally:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/yourusername/obskira-runway-deck.git
   git branch -M main
   git push -u origin main
   ```

### Deploy to Vercel (Recommended)
1. Sign up at vercel.com
2. Click "New Project" → Import GitHub repo
3. Select `obskira-runway-deck`
4. Click "Deploy"
5. Auto-deploys on every push to `main`

### Deploy to GitHub Pages
1. Go to repo Settings → Pages
2. Select `main` branch as source
3. Save — site goes live at `yourusername.github.io/obskira-runway-deck`

### Deploy to Netlify
1. Sign up at netlify.com
2. Click "New site from Git"
3. Connect GitHub, select repo
4. Leave build command blank, publish directory as `.`
5. Deploy

## Best Practices

### Commits
- Write clear commit messages
- Commit after logical changes (new section, styling update, etc.)
- Keep commits focused — one feature per commit

### Content Management
- Keep `index.html` organized with section comments
- Update this guide if project structure changes
- Backup sensitive data before major refactors

### Performance
- Optimize images before uploading (compress to <500KB each)
- Test locally before pushing (`npm run dev`)
- Monitor Vercel/Netlify analytics for performance metrics

### Accessibility
- Alt text for all images
- Semantic HTML (use `<section>`, `<header>`, `<p>` tags properly)
- Color contrast meets WCAG standards (dark background + light text)

## Troubleshooting

### Local server won't start
```bash
lsof -ti:8000 | xargs kill -9   # Kill existing process
npm run dev                      # Try again
```

### Changes not showing after push
- Wait 1-2 minutes for deployment
- Check Vercel/Netlify dashboard for build errors
- Clear browser cache (Cmd+Shift+Delete)

### Images not displaying
- Verify relative file paths (no leading `/`)
- Ensure images are committed to git
- Check file extensions (.jpg, .png)

### Git push rejected
```bash
git pull origin main             # Pull latest changes
git push origin main             # Push again
```

## Editor Settings

Recommended VS Code extensions:
- Live Server (optional, for quick preview)
- Prettier (code formatting)
- ES7+ React/Redux Snippets (not required but helpful)

## Collaboration Notes

- Keep `.gitignore` updated with temporary files
- Don't commit large binary files (images should be <5MB each)
- Use descriptive branch names if working with multiple contributors
- Test locally before pushing critical changes

---

**Last Updated:** March 2026  
**Status:** Ready for deployment  
**Maintainer:** OBSKIRA RUNWAY Team
