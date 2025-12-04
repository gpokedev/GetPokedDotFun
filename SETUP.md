# 🎮 Poké Game - Setup Guide

## 📋 What's New

Your Pokémon game now has a complete landing page system with:

1. **Landing Page** (`index.html`) - Main entry point with Start/Resume buttons
2. **Game Page** (`game.html`) - The actual Pokémon game
3. **Chart Page** (`chart.html`) - Live Solana chart (ready for your token)

---

## 🚀 Quick Start

### 1. Run Locally

```bash
# Navigate to project directory
cd pokemon

# Start local server
python -m http.server 8000

# Open in browser
# Visit: http://localhost:8000
```

### 2. What You'll See

- **Landing Page**: Beautiful pixel-art themed page with game buttons
- **Start Game**: Launches the Pokémon game
- **Resume Game**: Continues from last save (if available)
- **Live Chart**: Shows Solana real-time price chart
- **Social Links**: X (Twitter) and Pump.fun links
- **Contract Address**: Shows "TBA" until you deploy

---

## ⚙️ Customization

### Update Pump.fun Link

Edit `index.html` around line 262:

```javascript
// Replace this line:
document.getElementById('pumpfun-link').addEventListener('click', (e) => {
  e.preventDefault();
  alert('Pump.fun link coming soon!');
});

// With:
document.getElementById('pumpfun-link').href = 'YOUR_PUMPFUN_URL';
```

Or simply update the HTML directly:

```html
<a href="YOUR_PUMPFUN_URL" target="_blank" class="social-link" id="pumpfun-link">
```

### Update Contract Address

Edit `index.html` around line 252:

```html
<div class="contract-address">TBA</div>
```

Replace `TBA` with your actual contract address.

### Update Token Chart

Once your token launches, edit `chart.html` around line 274:

```javascript
// Replace this:
"symbol": "BINANCE:SOLUSDT",

// With your token's symbol, for example:
"symbol": "RAYDIUM:YOURTOKEN/SOL",
```

Also update the price fetching API calls to use your token's data instead of Solana.

---

## 🎨 Design Features

### Landing Page
- ✅ Animated gradient background with game map overlay
- ✅ Floating pixel particles
- ✅ Retro pixel font (Press Start 2P)
- ✅ Responsive design for mobile/desktop
- ✅ Hover animations on all buttons
- ✅ Game-themed color scheme (purple, gold, pink)

### Chart Page
- ✅ Real-time Solana price ticker
- ✅ TradingView embedded chart
- ✅ Live price statistics
- ✅ Auto-refresh every 30 seconds
- ✅ Dark theme matching game aesthetic

---

## 📱 Mobile Responsive

All pages are fully responsive and work on:
- 📱 Mobile phones
- 📱 Tablets
- 💻 Desktop computers

---

## 🔗 Navigation Flow

```
Landing Page (index.html)
    ├─→ Start Game → game.html
    ├─→ Resume Game → game.html (with saved state)
    ├─→ Live Chart → chart.html
    ├─→ X Account → https://x.com/getpokedotfun
    └─→ Pump.fun → (update with your link)

Chart Page (chart.html)
    ├─→ Play Game → game.html
    └─→ Back → index.html
```

---

## 🚀 Deployment

Your project is ready to deploy! See `DEPLOY.md` for full deployment instructions.

**Quick Deploy Options:**
1. **GitHub Pages** (recommended) - Already configured
2. **Netlify** - Drag & drop
3. **Vercel** - One command deploy

---

## 🎮 Game Features

The game (`game.html`) includes:
- Overworld exploration with WASD keys
- Random battle encounters
- Turn-based combat system
- NPC interactions
- Background music and sound effects
- Save/load functionality (localStorage)

---

## 📝 File Structure

```
pokemon/
├── index.html          # 🏠 Landing page (START HERE)
├── game.html           # 🎮 Main game
├── chart.html          # 📊 Live chart
├── index.js            # Game logic
├── battleScene.js      # Battle system
├── classes.js          # Game classes
├── SETUP.md           # This file
├── DEPLOY.md          # Deployment guide
└── [other game files]
```

---

## ✅ Checklist Before Launch

- [ ] Update Pump.fun link in `index.html`
- [ ] Update contract address in `index.html`
- [ ] Update token chart symbol in `chart.html`
- [ ] Test all buttons and links
- [ ] Test on mobile devices
- [ ] Deploy to hosting platform
- [ ] Update social media links if needed

---

## 🆘 Troubleshooting

### Game won't load
- Make sure you're using a local server (not just opening the file)
- Check browser console for errors (F12)

### Chart not showing
- TradingView widget requires internet connection
- Check if TradingView is blocked by ad-blocker

### Resume button not working
- This is normal if you haven't played yet
- The button activates after first game session

---

## 🎉 You're Ready!

Your Pokémon game landing page is complete and ready to deploy!

Visit `http://localhost:8000` to see it in action.

For deployment help, see `DEPLOY.md`.

---

**Need help?** Check the code comments in each HTML file for detailed instructions.








