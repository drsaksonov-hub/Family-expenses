# Family Expense Tracker PWA

A beautiful, full-featured Progressive Web App for tracking family expenses. Works offline, supports multiple input methods, and provides detailed visualizations.

## Features

### Input Methods
- **Manual Entry** - Type expense amount and description
- **Camera/Gallery** - Take photos of receipts or upload from gallery with OCR
- **Voice Input** - Speak your expenses naturally (e.g., "I spent 500 baht on groceries")
- **Statement Import** - Upload bank/credit card statements (CSV format)

### Multi-Currency Support
- Thai Baht (฿) - Primary currency
- US Dollars ($) - Auto-converts to THB at 35.5 rate
- Euros (€) - Auto-converts to THB at 38.2 rate

### Categories (Pre-populated for families)
🛒 Groceries | 🍽️ Dining Out | 🚗 Transport | 💡 Utilities
👶 Kids | 📚 Education | 🏥 Healthcare | 🎬 Entertainment
🛍️ Shopping | 🏠 Housing | 📱 Subscriptions | ✈️ Travel
💅 Personal | 🐕 Pets | 🎁 Gifts | 📌 Other

### Visualizations
- **Pie Chart** - Category breakdown
- **Bar Chart** - Daily spending
- **Line Chart** - 6-month trend

### Budget Management
- Set total monthly budget
- Set per-category budgets
- Visual progress bars
- Over-budget warnings

### Notifications
- Daily morning summary at customizable time
- Sends to all family members
- Shows spending vs. budget status

### Thai Language Support
- OCR supports Thai text on receipts
- Thai voice recognition
- Google Cloud Translation API integration for translating Thai receipts to English

---

## Free Hosting Recommendations

### Option 1: GitHub Pages (Recommended - Easiest)

1. Create a GitHub account at https://github.com
2. Create a new repository named `family-expenses`
3. Upload all files from this folder
4. Go to Settings → Pages → Source → Deploy from branch (main)
5. Your app will be live at: `https://yourusername.github.io/family-expenses`

### Option 2: Netlify (Very Easy)

1. Go to https://netlify.com and sign up
2. Drag and drop this entire folder to deploy
3. Get instant URL like: `https://random-name.netlify.app`
4. Optional: Connect custom domain

### Option 3: Vercel (Great for PWAs)

1. Go to https://vercel.com and sign up
2. Install Vercel CLI: `npm i -g vercel`
3. Run `vercel` in this folder
4. Follow prompts - get instant deployment

### Option 4: Cloudflare Pages (Fast & Free)

1. Go to https://pages.cloudflare.com
2. Connect GitHub repository or direct upload
3. Deploy with one click

---

## Adding to iPhone Home Screen

1. Open Safari and go to your hosted app URL
2. Tap the Share button (square with arrow pointing up)
3. Scroll down and tap **"Add to Home Screen"**
4. Name it "Family Expenses"
5. Tap **"Add"**

The app will appear as an icon on your home screen and launch in full-screen mode like a native app!

---

## Google Cloud Translation API Setup

To enable Thai-to-English translation for receipts:

1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Create a new project or select existing
3. Enable the **Cloud Translation API**
4. Go to **APIs & Services → Credentials**
5. Click **Create Credentials → API Key**
6. Copy the API key
7. In the app, go to **Settings** and paste your API key

**Note:** Google Cloud offers $300 free credit for new accounts. Translation costs ~$20 per million characters.

---

## File Structure

```
expense-tracker/
├── index.html      # Main app (all-in-one HTML/CSS/JS)
├── manifest.json   # PWA manifest for installation
├── sw.js          # Service Worker for offline support
├── icon-192.png   # App icon (192x192)
├── icon-512.png   # App icon (512x512)
└── README.md      # This file
```

---

## Data Storage

All data is stored locally in your browser's localStorage:
- `familyExpenses` - All expense records
- `familyBudgets` - Category budgets
- `familySettings` - App settings

**Export:** Go to Settings → Export Data to download CSV
**Clear:** Go to Settings → Clear All Data to reset

---

## Browser Support

- ✅ Safari (iOS 11.3+)
- ✅ Chrome (Android/Desktop)
- ✅ Firefox
- ✅ Edge

Voice input requires browser microphone permission.
Camera requires browser camera permission.

---

## Tips for Use

1. **Quick Entry:** Tap the + button at the bottom for fastest expense entry
2. **Receipt Scanning:** Works best with clear, well-lit photos
3. **Voice Commands:** Speak naturally - "Lunch was 350 baht" or "Spent 500 on groceries"
4. **Budget Alerts:** Set budgets to get visual warnings when overspending
5. **Daily Review:** Check the morning notification to stay on track

---

## Troubleshooting

**App not installing?**
- Make sure you're using Safari on iOS or Chrome on Android
- The site must be served over HTTPS

**OCR not working?**
- Ensure good lighting when photographing receipts
- Try the gallery option for clearer images

**Voice not recognized?**
- Check microphone permissions in browser settings
- Speak clearly and include numbers

**Translation not working?**
- Verify your Google API key in Settings
- Check that the Cloud Translation API is enabled

---

Made with ❤️ for families managing their finances together
