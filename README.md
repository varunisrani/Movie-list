# Movie List

Movie List is a React browser for discovering and searching movie and television metadata from The Movie Database (TMDB).

## Core features

- Movie and television discovery grids populated from TMDB.
- Detail routes for selected movies and TV shows.
- Text search for both movies and TV content.
- Browser speech-recognition input for supported search pages.
- Navigation between movie, TV, search, and voice-oriented views.
- Online/offline status assets and UI experiments included in the source tree.

## Technology stack

- React 18 and React Router 6
- Vite 5 with the React SWC plugin
- JavaScript/JSX and Tailwind CSS 3
- Material UI icons, Lottie, and React Toastify
- TMDB HTTP API and browser Web Speech APIs

## Prerequisites

- Node.js compatible with the locked dependencies
- npm
- Network access to TMDB for catalog data and images
- A browser with Web Speech API support for voice search

## Local setup

```bash
git clone https://github.com/varunisrani/Movie-list.git
cd Movie-list
npm ci
npm run dev
```

Build and inspect the production bundle with:

```bash
npm run build
npm run preview
```

Lint the project with `npm run lint`.

## Configuration

The source does not currently read environment variables. TMDB access is configured directly in the client source rather than through an environment variable.

## Project structure

- `src/main.jsx` — application entry point
- `src/components/Approuter.jsx` — browser routes
- `src/components/Moviemain.jsx` and `Tv.jsx` — discovery views
- `src/components/Search.jsx` and `Search1.jsx` — movie and TV search
- `src/components/Movie.jsx` and `Maintv.jsx` — detail views
- `src/components/Voice.jsx` — voice-search experiment
- `src/components/*.json` — online/offline Lottie data

## Status and limitations

This is a front-end learning project. TMDB credentials are embedded in client code and should be rotated and moved to a safer configuration or server-side proxy before deployment. API failures have limited user-facing handling, voice search depends on non-standard browser APIs and microphone permission, and some labels do not precisely match the TMDB fields they display.
