# MovieReview (TMDB Trending + Favorites)

A React web app that surfaces weekly trending movies using The Movie Database (TMDB) API.  
Users can browse titles, paginate through results, and maintain a personal favorites list with filtering and sorting.

## Features
- **Trending Movies Feed**: Pulls weekly trending movies from TMDB.
- **Pagination**: Browse across pages of results.
- **Favorites / Watchlist**
  - Add/remove movies to favorites.
  - Persisted in **localStorage**.
- **Favorites Controls**
  - Filter by genre.
  - Search by movie title.
  - Sort by rating and popularity.
  - Paginated favorites table.
- **Clean UI** with hover actions and responsive layout.

## Tech Stack
- React (Create React App)
- React Router
- Axios
- Tailwind-style utility CSS classes (in components)
- TMDB API

## Project Structure
```
src/
  components/
    Banner.js
    Movies.js
    Favourites.js
    NavBar.js
    Pagination.js
  App.js
  index.js
```

## Getting Started

### 1. Clone & Install
```bash
git clone <your-repo-url>
cd movieReview-main
npm install
```

### 2. Run Locally
```bash
npm start
```
App runs on: `http://localhost:3000`

## API Notes
The app calls TMDB’s trending endpoint:
- `GET https://api.themoviedb.org/3/trending/movie/week`
- API key is currently embedded in the code.  
  **Recommended improvement:** move to `.env`:
```bash
REACT_APP_TMDB_KEY=your_key_here
```
Then update requests to use:
```js
process.env.REACT_APP_TMDB_KEY
```

## Future Improvements
- Add detail page for each movie.
- Replace embedded API key with environment variables.
- Add debounce to search on favorites page.
- Add loading skeletons + error UI.
