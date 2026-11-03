# Album Tracker

Album Tracker is a React web app for finding music albums, previewing their tracks, and keeping a personal listening log. You can search albums and artists, play 30-second previews in a mini player, save albums with a status, star rating, and notes, open full albums on Deezer, and get AI-powered recommendations based on your own collection.

**Live site:** https://album-tracker-of1z.vercel.app

<img width="1911" height="991" alt="Album Tracker Screenshot" src="https://github.com/user-attachments/assets/dc2df016-72ea-41a6-a221-eb8faf3865ba" />



## Features

- Search albums and artists with the iTunes Search API
- Album page with cover, year, genre, track list, and links to Spotify, YouTube, and Apple Music
- Mini player with play/pause, previous/next, and a seek bar that keeps playing while you browse
- Personal collection with statuses (Want to listen, Listening, Listened), 1-5 star ratings, and notes
- Filter and sort your collection by status, title, artist, or rating
- Optional full-album playback with Deezer's embedded player
- LLM-powered recommendations based on the user's saved albums and ratings

## Tech Stack

React, Vite, Context API, iTunes Search API, Deezer, Google Gemini API, and Vercel (hosting and serverless functions).

## Run It Locally

1. Clone the repository and open the folder.
2. Install dependencies:
   ```
   npm install
   ```
3. Create a file named `.env.local` in the project root with your own Gemini API key:
   ```
   GEMINI_API_KEY=your-key-here
   ```
4. Start the dev server:
   ```
   npm run dev
   ```
5. Open the address it prints (usually http://localhost:5173).

## Limitations

- Previews are 30 seconds, because that is all the iTunes API provides.
- Your collection is saved only in your browser (localStorage), so it does not sync between devices.
- Deezer needs you to be logged in, with a plan that includes full tracks in your country, to play full albums. Otherwise it plays previews only.
- AI recommendations depend on the Gemini free tier and may hit rate limits.

## Privacy

The recommendations feature sends your saved albums' titles, artists, ratings, and statuses to Google's Gemini API. Your notes are not sent. The API key is stored only as a server-side environment variable and is never in the browser code or this repository.

## Disclaimer

This is a learning project and is not affiliated with Apple, Spotify, Deezer, or Google. Music data, artwork, and audio belong to their owners.
