# PawLog / Paw-Plan

PawLog is a mobile-first prototype designed for owners of high-energy or overwhelming dogs. It creates a quick daily plan using the dog’s saved issues, goals, current energy, available time and activity preferences.

## Current prototype features

- One-time owner and dog setup with editable owner name, dog name, weight, breed, age, size and energy level.
- Saved issues, short-term goals and long-term goals.
- Returning four-digit login experience with no username shown on the welcome-back screen.
- Browser-based password-recovery prototype using the saved email address.
- Daily check-in designed to take under 30 seconds.
- At least three personalised activities, scored against saved issues and goals.
- Activity library with category, location and difficulty filters.
- Each activity explains the goal/issue it supports and includes equipment and steps.
- “Add to today” adds an activity without navigating away from the library.
- Small tick/cross feedback controls. Likes promote similar activities; dislikes reduce similar recommendations.
- Profile menu with separate buttons for owner/dog details, activity preferences, issues/goals and settings.
- Clearly separated liked and disliked activity history.
- Progress history for completed activities, generated plans, positive days and behaviour notes.
- Mobile/iPhone-friendly responsive layout and installable web-app manifest.

## Run locally

This is a static app with no build step. Open `index.html` in a browser, or serve the folder with any static web server.

For example:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy

The repository includes `netlify.toml`, so Netlify can publish the repository root directly with no build command.

## Prototype data and security

The current version stores profile data and the four-digit login code in `localStorage`. Password recovery opens the user’s email client with a generated recovery code. This is suitable for a prototype only. Before production, authentication, password recovery and user data should be moved to a secure backend (for example Supabase or another authenticated database/service), with proper password hashing, server-side email delivery, access controls and privacy handling.

## Product naming

The repository is named **Paw-Plan** while the current app UI uses **PawLog**, matching the latest prototype iteration. The name can be standardised later without changing the repository history.
