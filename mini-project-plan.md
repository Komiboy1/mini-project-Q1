# Mini Project Plan: Movie/TV Explorer

## Description

A web app where users can search for movies and TV shows and see key details
— poster, title, release year, rating, and overview — pulled live from the
TMDb (The Movie Database) API. It's for anyone who wants a quick, no-login
way to look up information on a film or show.

## Features

### Must-Have (Core)
- Search bar that queries the TMDb API for movies/TV shows
- Results displayed as a grid: poster, title, release year, rating
- Clicking a result shows a detail view (overview, genre, rating, release date)
- Loading state while a search is in progress
- Empty/no-results state when a search returns nothing
- At least 2 pure JavaScript functions covered by Jest tests (e.g. rating
  formatter, date formatter, or a result sorter/filter)

### Nice-to-Have (Stretch)
- Toggle between "Movies" and "TV Shows"
- Genre filter or sort by rating/date
- "Trending this week" section shown on page load, before any search
- Favorites list (stored in localStorage)
- Debounced search-as-you-type instead of a submit button

## Tech Stack

- HTML, CSS, JavaScript (no framework)
- TMDb API for movie/TV data (requires a free API key from themoviedb.org)
- Jest for unit tests on pure logic functions (formatters, sorters — not
  DOM/fetch code)
- Deployed as a static site on GitHub Pages

## Layout Sketch

- **Header:** app title + search bar
- **Body:** grid of result cards, each showing poster, title, year, rating
- **Detail view:** clicking a card opens a panel/modal with overview, genre,
  release date, and rating

## Acceptance Criteria

- User can search and see relevant movie/TV results with posters
- User can click into a result and see more detail
- App handles empty search and no-results states gracefully
- At least 2 Jest tests exist and pass for pure logic functions
- Project is deployed on GitHub Pages and verified working on the live URL

## Risks

- TMDb API key signup could take time — get this set up on day one
- Some titles may be missing poster images — need a fallback/placeholder
- Detail view could scope-creep (cast lists, trailers, similar titles) —
  must-have scope is limited to overview + rating + genre only
- Rate limits on the TMDb free tier during heavy testing (low risk, worth
  being aware of)