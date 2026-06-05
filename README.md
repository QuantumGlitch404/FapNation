# FapNation - Ultimate Adult Video Browser

**FapNation** is a sleek, high-performance, fully responsive web application designed for seamless browsing of premium adult content. It leverages the powerful **Eporner API** to fetch and display videos directly from Eporner's high-quality servers, allowing users to enjoy videos in resolutions up to 4K and beyond without any hosting burden on this platform.

**⚠️ STRICTLY 18+ ONLY** - This project contains explicit adult material. Access is restricted to adults aged 18 or older (or the legal age of majority in your jurisdiction). Minors are strictly prohibited.

![FapNation Logo](img/Fap-tap.png)

## ✨ Key Features

- **Multi-Filter Search System**:
  - **Keyword Search** (default): Search by any term, actor, title, or phrase.
  - **Category Browsing**: Browse popular categories like Amateurs, Anal, Big Ass, Big Tits, Blowjob, MILF, Teens, Hentai, Interracial, and dozens more.
  - **Duration Filter**: Toggle between Short Videos and Long Videos (longest videos available).
  - **Section Filter**: Straight (Hetero), Gay, Trans, Lesbian content separation.

- **Infinite Pagination**: Navigate up to 100 pages of content (30 videos per page).

- **Dynamic Hover Previews**:
  - On desktop: Hover over any thumbnail to see a smooth cycling preview of multiple frames from the video.
  - On mobile: Tap and hold on the thumbnail for the same preview experience.

- **Dedicated Pages**:
  - **Home**: Latest releases with the freshest content.
  - **Trending**: Weekly top-performing videos (updated automatically via Eporner’s `top-weekly` order).

- **High-Quality Thumbnails & Metadata**:
  - Eye-catching thumbnails with view counts and video durations displayed.
  - Truncated but informative titles.
  - Direct embed links to Eporner player for instant high-res playback.

- **Fully Responsive Design**:
  - Optimized for desktop, tablet, and mobile devices.
  - Smooth animations, dark theme, modern card-based UI.

- **Fast Loading & UX**:
  - Loading spinner during API calls.
  - Keyboard support (Enter key for searches).
  - Smooth scrolling and intuitive navigation.

- **Privacy-Focused**:
  - No user accounts, no tracking beyond basic analytics.
  - All content embedded from Eporner – no direct hosting.

## 🛠️ Tech Stack

- **Frontend**:
  - HTML5, CSS3 (custom responsive stylesheets)
  - Vanilla JavaScript (no frameworks for maximum performance)
  - Bootstrap 5 components for layout and responsiveness

- **API Integration**:
  - Eporner Video Search API v2 (`https://www.eporner.com/api/v2/video/search/`)
  - Supports parameters: `query`, `page`, `per_page`, `order`, `lq`, `gay`, etc.

- **Fonts**:
  - Gotham Black (headings)
  - PT Sans Bold (titles)

- **Assets**:
  - Custom icons for views, duration, trending (campfire emoji style)

- **Deployment**:
  - Static hosting ready (Vercel, Netlify, GitHub Pages, etc.)
  - Live demo: [https://fapnation.vercel.app/](https://fapnation.vercel.app/)

## 📁 Project Structure

```
FapNation-main/
├── index.html                 # Main homepage
├── best.html                  # Alternative/trending-focused page
├── terms&privacy.html         # Legal pages
├── JS/
│   └── main.js                # Core JavaScript logic
├── style/
│   ├── stylesheet.css         # Primary dark/orange theme
│   └── testcss.css            # Alternative blue theme (for experimentation)
├── fonts/
│   ├── Gotham-Black.otf
│   └── PTSans-Bold.ttf
├── img/
│   ├── Fap-tap.png            # Logo
│   ├── campfire.png           # Trending icon
│   ├── eye.png                # Views icon
│   ├── clock-circular-outline.png # Duration icon
│   └── no-minors.png          # Age warning
└── README.md                  # This file
```

## 🚀 Installation & Local Setup

1. **Clone or Download**:
   ```bash
   git clone <your-repo-url>
   # or download and extract FapNation-main.zip
   ```

2. **Serve Locally**:
   - Use any static server:
     ```bash
     # Python
     python -m http.server 8000
     
     # Node.js (with serve)
     npx serve
     
     # Or open index.html directly in browser
     ```

3. **Open in Browser**:
   - Navigate to `http://localhost:8000`
   - Start fapping immediately!

**Note**: Since it's a static site with API calls, no backend or database setup required.

## 🔧 How It Works

### Search Logic (`main.js`)

- `tipoRicerca` variable controls the active filter (1=Category, 2=Keyword, etc.).
- `Ricerca()` function constructs appropriate Eporner API URLs based on selection.
- `stampaCards()` renders video cards with hover/ touch handlers.
- `CreaHome()` and `CreaTrending()` for dedicated pages.

### Hover Preview System

```javascript
// Cycles through thumbnail frames every 350ms
function CambiaImmagineOnHover(cardElement, thumbBase) { ... }
```

Thumbnails follow Eporner naming like `1_`, `2_`, ..., `15_` for previews.

### Pagination

- `pagina` state (1-100)
- Next/Previous buttons update content and maintain filter state.

## 🎨 Customization

- **Themes**: Switch between `stylesheet.css` (orange accents) and `testcss.css` (blue accents) by updating links in HTML.
- **Categories**: Edit options in `<select id="categoria">` in HTML files.
- **API Tweaks**: Modify base URLs or parameters in `main.js` for different sorting (latest, top-weekly, etc.).
- **Per Page**: Change `per_page=30` to higher/lower values.

## ⚖️ Legal & Disclaimer

- **Content Ownership**: All videos belong to their respective creators and are hosted on Eporner.com. FapNation is purely an aggregator/interface.
- **DMCA**: We respect copyright. Contact for removal requests.
- **Age Gate**: Strong emphasis on 18+ compliance.
- **No Liability**: Provided "as is". Use at your own risk. We are not responsible for content accessed via third-party embeds.

See `terms&privacy.html` for full details.

## 📈 Roadmap / Future Enhancements

- Video player integration directly on site (with Eporner embed improvements).
- Favorites/watchlist using localStorage.
- Advanced filters (quality, HD/4K only, specific actors).
- Dark/Light mode toggle.
- Infinite scroll instead of pagination.
- Search history and suggestions.
- Multi-language support.
- PWA capabilities for offline thumbnail caching.

## 🤝 Contributing

Contributions welcome! Especially:

- Bug fixes in JS API handling.
- UI/UX improvements.
- Additional themes or accessibility features.
- Performance optimizations.

1. Fork the repo
2. Create a feature branch
3. Submit PR with detailed description

## 📬 Contact & Support

- **Developer**: QuantumGlitch404
- **Live Site**: https://fapnation.vercel.app/
- **Issues**: Open GitHub issues for bugs or feature requests.

## ⭐ Star This Repo

If this project helps you find quality fap material efficiently, please star it! Your support keeps the development going.

---

**Made with pure lust for high-quality porn browsing experience.**

**Unleash your inner degenerate responsibly.**

**© 2025 FapNation. All Rights Reserved.**
