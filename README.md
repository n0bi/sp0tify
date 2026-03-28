# Spotify Remote Dashboard

This is a browser-based Spotify dashboard for Android or desktop. It uses Spotify's Web Playback SDK plus the Authorization Code with PKCE flow.

## What it does
- shows album art, track name, artist, and album
- previous / play-pause / next buttons
- volume slider
- signs in with your own Spotify account
- creates a Spotify Connect device in the browser

## What you need
- Spotify Premium
- your own Spotify developer app Client ID
- a real page URL hosted over HTTPS, or `http://127.0.0.1` for local testing

## Setup
1. Host `spotify_dashboard.html` somewhere with HTTPS.
2. Open the page once and copy the exact Redirect URI shown in the page.
3. In the Spotify Developer Dashboard, create an app.
4. Add that exact Redirect URI to the app settings.
5. Open the page again, paste your Client ID, and tap **Save settings**.
6. Tap **Sign in with Spotify**.
7. After you return, tap **Activate audio**.
8. Tap **Use this device**.
9. If playback does not start immediately, start a track once in Spotify and tap **Use this device** again.

## Personal-use setup
If you only want this to work with your account, keep the app in Spotify Development Mode and only authorize your own account.

## Notes
- Client IDs are public. Do not paste your Client Secret into this page.
- The page stores tokens in browser localStorage for convenience.
- To fully reset it, use the Sign out button and clear site storage in your browser if needed.
