# Anime Streaming Platform

A modern, legal anime streaming platform built with React, TypeScript, and Tailwind CSS.

## 🌟 Features

- ✅ **Clean, Modern UI** - Professional design with consistent styling
- ✅ **No Ratings System** - Replaced with popularity and view counts
- ✅ **Responsive Design** - Works perfectly on mobile, tablet, and desktop
- ✅ **Fast Navigation** - React Router for smooth page transitions
- ✅ **Search & Filter** - Find anime by title, genre, status, and type
- ✅ **Video Player Page** - Dedicated watch page with episode navigation
- ✅ **Download Support** - Structure ready for legal episode downloads
- ✅ **Episode Management** - Browse and select episodes easily

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Start Development Server**
   ```bash
   npm run dev
   ```

3. **Open in Browser**
   ```
   http://localhost:5173
   ```

### Build for Production

```bash
npm run build
```

## 📁 Project Structure

```
vite-react-main/
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── Navbar.tsx
│   │   ├── AnimeCard.tsx
│   │   ├── HeroSection.tsx
│   │   └── AnimeRow.tsx
│   ├── pages/              # Page components
│   │   ├── HomePage.tsx
│   │   ├── BrowsePage.tsx
│   │   ├── AnimeDetailPage.tsx
│   │   ├── WatchPage.tsx
│   │   └── SearchPage.tsx
│   ├── types/              # TypeScript type definitions
│   ├── data/               # Mock data for development
│   ├── App.tsx             # Main app with routing
│   └── index.css           # Global styles with Tailwind
```

## 📄 Pages

- **Home** (`/`) - Hero section and content rows
- **Browse** (`/browse`) - Filterable anime grid
- **Anime Detail** (`/anime/:id`) - Full anime information and episodes
- **Watch** (`/watch/:id/:episodeNumber`) - Video player with episode navigation
- **Search** (`/search`) - Search results

## ⚖️ Legal Compliance

This template is designed for LEGAL anime streaming only:

1. ✅ Obtain proper licensing for all content
2. ✅ Implement DMCA/Copyright policy
3. ✅ Never scrape or rehost pirated content

## 🛠️ Tech Stack

- React 18 + TypeScript
- Vite
- React Router
- Tailwind CSS
- Lucide React (icons)

---

**Important**: Only use with properly licensed content.
