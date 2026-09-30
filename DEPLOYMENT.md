# ReLens App - Live Deployment Guide

## 🚀 Quick Start: GitHub Pages (Free, Zero Cost)

Your app is **automatically deployed** whenever you push to the `main` branch.

### Access Your Live Site
```
https://Relensservice.github.io/Relensapp/
```

---

## 📋 What's Included

### 1. **Progressive Web App (PWA) Setup**
- ✅ `manifest.webmanifest` - App metadata for installation
- ✅ `sw.js` - Service worker for offline support
- ✅ `index.html` - Main application

### 2. **Automatic Deployment**
- GitHub Actions workflow automatically deploys on every push to `main`
- No manual steps required
- Zero cost hosting

### 3. **CI/CD Validation**
- HTML validation on every commit
- Manifest JSON syntax checking
- Service worker verification

---

## 🔧 Deployment Flow

```
git push to main
    ↓
GitHub Actions triggers
    ↓
Runs validation checks
    ↓
Builds & deploys to GitHub Pages
    ↓
Live at https://Relensservice.github.io/Relensapp/
```

---

## 📱 Installing as a Mobile App

1. Open the site in a mobile browser:
   - **iOS**: Safari → Share → Add to Home Screen
   - **Android**: Chrome → Menu (⋮) → "Install app"

2. The app will:
   - Run full-screen like a native app
   - Work offline with cached assets
   - Support push notifications (if added)

---

## 🎨 Customization

### Change Site Metadata
Edit `manifest.webmanifest`:
```json
{
  "name": "Your App Name",
  "short_name": "Short Name",
  "start_url": "./",
  "display": "standalone"
}
```

### Add Custom Domain
Go to **Settings → Pages → Custom Domain** and enter your domain:
- Point your domain's DNS to GitHub Pages
- Example: `relens.app` instead of `Relensservice.github.io/Relensapp/`

### Cache Busting
Edit `sw.js` service worker version:
```javascript
const V = 'relens-v2'; // Change version to bust cache
```

---

## 🖼️ Missing Icons (Optional but Recommended)

Add these 3 PNG icons to the root directory for full PWA support:

1. **icon-192.png** (192×192 px) - Android home screen
2. **icon-512.png** (512×512 px) - Large app icon  
3. **icon-maskable.png** (512×512 px) - Adaptive icon for iOS

The manifest already references these. Once added, the app will be fully installable.

---

## 📊 Monitor Deployment

1. Go to **Actions** tab on GitHub
2. Watch the `Deploy to GitHub Pages` workflow
3. Green ✅ = Live
4. Red ❌ = Check logs for errors

---

## 🌐 Alternative Hosting Options

| Platform | Cost | Setup Time | Custom Domain |
|----------|------|-----------|---|
| **GitHub Pages** | Free | 2 min | Yes |
| Netlify | Free | 5 min | Yes |
| Vercel | Free | 5 min | Yes |
| Firebase Hosting | Free tier | 10 min | Yes |
| AWS S3 + CloudFront | ~$1/mo | 20 min | Yes |

### Switch to Netlify (Optional)
1. Go to [netlify.com](https://netlify.com)
2. Connect your GitHub repo
3. Deploy with one click (auto-deploys on push)
4. Add custom domain in Netlify settings

---

## ✅ Deployment Checklist

- [x] PWA manifest configured
- [x] Service worker active
- [x] GitHub Pages enabled (auto-enabled for public repos)
- [x] CI/CD validation pipeline running
- [ ] Add icon PNGs (optional)
- [ ] Set custom domain (optional)
- [ ] Test offline functionality
- [ ] Monitor performance

---

## 📞 Support

**Live Site**: https://Relensservice.github.io/Relensapp/  
**Repo**: https://github.com/Relensservice/Relensapp  
**Actions**: https://github.com/Relensservice/Relensapp/actions

---

## 🔐 Security & Performance

- **HTTPS**: Automatic with GitHub Pages
- **Caching**: Service worker caches key assets
- **Performance**: Tailwind CDN + lazy loading
- **Mobile**: Responsive design included

Your app is production-ready! 🎉
