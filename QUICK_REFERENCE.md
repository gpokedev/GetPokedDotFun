# 🎮 Quick Reference Card

## 🌐 Your Website is Live!

**Visit:** http://localhost:8000

---

## 📄 Pages

| Page | URL | Description |
|------|-----|-------------|
| 🏠 Landing | `index.html` | Main entry with Start/Resume/Chart buttons |
| 🎮 Game | `game.html` | The Pokémon game |
| 📊 Chart | `chart.html` | Live Solana chart (ready for your token) |

---

## ⚙️ Quick Edits

### 1. Update Pump.fun Link
**File:** `index.html` (line 262)
```javascript
document.getElementById('pumpfun-link').href = 'YOUR_PUMPFUN_URL';
```

### 2. Update Contract Address
**File:** `index.html` (line 252)
```html
<div class="contract-address">YOUR_CONTRACT_HERE</div>
```

### 3. Update Token Chart
**File:** `chart.html` (line 274)
```javascript
"symbol": "RAYDIUM:YOURTOKEN/SOL",
```

---

## 🚀 Deploy Commands

### GitHub Pages
```bash
git add .
git commit -m "Add landing page"
git push origin master
# Enable Pages in repo settings
```

### Netlify (Drag & Drop)
Visit: https://app.netlify.com/drop
Drag your `pokemon` folder

### Vercel
```bash
vercel
```

---

## 🎨 What's Included

✅ Start Game button → launches game  
✅ Resume Game button → continues from save  
✅ Live Chart button → shows Solana chart  
✅ X Account link → https://x.com/getpokedotfun  
✅ Pump.fun logo → clickable (update link)  
✅ Contract Address → shows "TBA"  
✅ Game-themed background → pixel art style  
✅ Mobile responsive → works on all devices  

---

## 📱 Test Checklist

- [ ] Visit http://localhost:8000
- [ ] Click "Start Game" → should load game
- [ ] Click "Resume Game" → should load game
- [ ] Click "Live Chart" → should show Solana chart
- [ ] Click X link → should open Twitter
- [ ] Test on mobile (resize browser)

---

## 🆘 Need Help?

- **Setup Guide:** See `SETUP.md`
- **Deploy Guide:** See `DEPLOY.md`
- **Full Summary:** See `LANDING_PAGE_SUMMARY.md`

---

## 🎉 You're All Set!

Your landing page is ready to go live! 🚀






