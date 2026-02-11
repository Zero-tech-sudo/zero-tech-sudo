# SETUP GUIDE - Anime Streaming Platform

## 📋 Quick Start (5 minutes)

### Step 1: Install Dependencies

Open your terminal in the project folder and run:

```bash
npm install
```

This will install:
- react & react-dom
- react-router-dom (for navigation)
- lucide-react (for icons)
- tailwindcss (for styling)
- TypeScript & Vite

### Step 2: Start Development Server

```bash
npm run dev
```

You'll see output like:
```
VITE v5.4.1  ready in 500 ms

➜  Local:   http://localhost:5173/
➜  Network: use --host to expose
```

### Step 3: Open in Browser

Visit: http://localhost:5173

You should see the anime streaming platform with:
- Home page with featured anime
- Navigation bar
- Multiple content sections
- All pages working with routing

## 🎯 What's Included

### Pages (All Fully Built)
✅ Home Page - Hero section + content rows
✅ Browse Page - Filters + anime grid
✅ Anime Detail Page - Full info + episodes
✅ Watch Page - Video player + controls
✅ Search Page - Search results

### Components (Ready to Use)
✅ Navbar - Search, navigation, mobile menu
✅ AnimeCard - Reusable anime card with hover effects
✅ HeroSection - Featured anime banner
✅ AnimeRow - Horizontal scrolling sections

### Features
✅ Responsive design (mobile, tablet, desktop)
✅ Dark theme
✅ Mock data for testing
✅ TypeScript types
✅ Tailwind styling

## 🔧 Customization

### Replace Mock Data with Your API

**File**: `src/data/mockData.ts`

Option 1 - Simple replacement:
```typescript
export const mockAnimeList = [
  // Replace with your data
];
```

Option 2 - Fetch from API:
```typescript
// Create a new file: src/api/anime.ts
export async function fetchAnimeList() {
  const res = await fetch('https://your-api.com/anime');
  return res.json();
}

// In your components:
import { fetchAnimeList } from '../api/anime';

const [animes, setAnimes] = useState([]);

useEffect(() => {
  fetchAnimeList().then(setAnimes);
}, []);
```

### Add Real Video Player

**File**: `src/pages/WatchPage.tsx`

Replace the placeholder section with:

```typescript
// Option 1: HTML5 Video
<video
  src={currentEpisode.streamAssets[0].streamUrl}
  controls
  className="w-full h-full"
  autoPlay
/>

// Option 2: Video.js (install first: npm install video.js)
import videojs from 'video.js';
import 'video.js/dist/video-js.css';

// Option 3: React Player (install: npm install react-player)
import ReactPlayer from 'react-player';

<ReactPlayer
  url={currentEpisode.streamAssets[0].streamUrl}
  controls
  width="100%"
  height="100%"
/>
```

### Change Colors/Theme

**File**: `tailwind.config.js`

```javascript
theme: {
  extend: {
    colors: {
      primary: {
        // Change these to your brand colors
        500: '#0ea5e9',
        600: '#0284c7',
        700: '#0369a1',
      },
    },
  },
},
```

## 📦 Building for Production

```bash
npm run build
```

This creates optimized files in the `dist` folder.

To preview the production build:
```bash
npm run preview
```

## 🚀 Deployment

### Deploy to Vercel (Recommended)

1. Push code to GitHub
2. Go to https://vercel.com
3. Click "Import Project"
4. Select your repository
5. Click "Deploy"

### Deploy to Netlify

1. Build the project: `npm run build`
2. Drag and drop the `dist` folder to Netlify
3. Done!

## 🐛 Common Issues

### "Module not found" errors

Run:
```bash
rm -rf node_modules package-lock.json
npm install
```

### Styles not loading

Make sure Tailwind is configured:
```bash
# Check these files exist:
- tailwind.config.js
- postcss.config.js
- src/index.css (has @tailwind directives)
```

### Router not working in production

Add to `vite.config.ts`:
```typescript
export default defineConfig({
  plugins: [react()],
  base: '/', // Important for routing
})
```

## 📁 File Structure Explained

```
src/
├── components/        # Reusable UI pieces
│   ├── Navbar.tsx          # Top navigation
│   ├── AnimeCard.tsx       # Individual anime card
│   ├── HeroSection.tsx     # Large banner section
│   └── AnimeRow.tsx        # Horizontal scrolling row
│
├── pages/            # Full pages (routes)
│   ├── HomePage.tsx        # / route
│   ├── BrowsePage.tsx      # /browse route
│   ├── AnimeDetailPage.tsx # /anime/:id route
│   ├── WatchPage.tsx       # /watch/:id/:ep route
│   └── SearchPage.tsx      # /search route
│
├── types/            # TypeScript definitions
│   └── index.ts            # Anime, Episode, User types
│
├── data/             # Data management
│   └── mockData.ts         # Sample data for testing
│
├── App.tsx           # Main app + routing setup
├── main.tsx          # Entry point
└── index.css         # Global styles + Tailwind
```

## 🎨 Design System

### Colors
- Primary Blue: `bg-primary-600`
- Dark Background: `bg-dark-950`
- Card Background: `bg-dark-900`
- Text: `text-dark-50` (light), `text-dark-400` (muted)

### Buttons
```tsx
<button className="btn-primary">Primary Action</button>
<button className="btn-secondary">Secondary Action</button>
```

### Cards
```tsx
<div className="card">
  {/* Your content */}
</div>
```

### Inputs
```tsx
<input className="input-field" placeholder="Search..." />
```

## 🔒 Before Going Live

1. **Remove Mock Data** - Replace with real API
2. **Add Authentication** - User login/signup
3. **Content License** - Ensure legal rights to all anime
4. **Add Policies**:
   - Terms of Service
   - Privacy Policy
   - DMCA Policy
5. **Set up CDN** - For video delivery
6. **Add Analytics** - Google Analytics, etc.
7. **Error Tracking** - Sentry, LogRocket, etc.

## 📞 Need Help?

Check these files:
- `README.md` - Project overview
- `SETUP_GUIDE.md` - This file
- `package.json` - Dependencies list

## ✅ Checklist

Before coding:
- [ ] Run `npm install`
- [ ] Run `npm run dev`
- [ ] Check http://localhost:5173
- [ ] Browse all pages
- [ ] Try search and filters

Ready to customize:
- [ ] Replace mock data
- [ ] Add real video player
- [ ] Customize colors/branding
- [ ] Add your logo
- [ ] Configure API endpoints

Ready for production:
- [ ] Remove console.logs
- [ ] Add error handling
- [ ] Test on mobile
- [ ] Build and preview
- [ ] Deploy to hosting

---

**You're all set!** Start by running `npm install` and `npm run dev`. The platform will be running locally and you can start customizing it.
