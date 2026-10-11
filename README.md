# Cavalier Rifle and Pistol Club

Modern redesign of the club's website — static HTML/CSS/JS, no build step required.

## Pages

- `index.html` — Home
- `facilities.html` — Ranges and grounds
- `membership.html` — How to join
- `matches.html` — Public and club matches
- `events.html` — Upcoming events (syncs with the club's Google Calendar — see below)
- `directions.html` — Address and map link
- `contact.html` — Contact form (front-end only; needs a mail service to actually send)
- `members-only.html` — Placeholder for a future member login

## Live calendar sync

`events.html` can pull events directly from the club's public Google Calendar
(`cavrpc@gmail.com`) at run time. To turn it on:

1. In [Google Cloud Console](https://console.cloud.google.com/), create a project
   (or use an existing one) and enable the **Google Calendar API**.
2. Create an API key (Credentials → Create Credentials → API key). Restrict it
   to the Calendar API and to this site's domain.
3. Open `events.html`, find `GCAL_API_KEY = ''` near the bottom of the file,
   and paste the key in.

Until a key is set, the page shows a static snapshot of upcoming events instead.

## Deployment

Served as-is via GitHub Pages from the repository root.
