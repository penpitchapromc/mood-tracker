# Mood Tracker Specification

## Goal

A simple, personal web app for recording a mood quickly whenever the user wants to. It is intended for one person and should be straightforward for someone new to web development to run and understand.

## Design direction

- Selected concept: **The Journal** from `designs.html` (the warm, reflective first design).
- Carry forward its calm palette, journal-like heading, compact mood picker, rating scale, optional note, and recent check-ins.
- This design direction should guide the initial implementation.

## Platform and data

- Build as plain web pages using HTML, CSS, and browser JavaScript; no server, account, or database service is required.
- Save entries in this browser on this device using browser storage.
- Do not send mood data to a remote service or add cross-device synchronization.
- Tell the user in the interface that entries are saved in this browser. Clearing browser site data or changing browsers/devices can remove or make entries unavailable.

## Check-in

- Let the user save multiple check-ins on the same day.
- Each check-in contains a named mood, a rating from 1 to 5, an automatically captured current date and time, and an optional text note.
- Keep the main check-in flow short: choose the mood, choose the rating, optionally enter a note, and save.
- Do not require a note.
- Capture the date and time when the user saves the entry. Do not offer backdating in the initial version.
- Show a clear confirmation when a check-in is saved.

## Mood choices and rating

- The user wants both a named mood and a numerical rating.
- Provide a small, fixed set of named moods that can be selected quickly. Initial suggested choices: Happy, Calm, Okay, Sad, Anxious, and Irritated.
- Keep the 1–5 rating separate from the mood label. Label the endpoints so the scale is easy to interpret (1 = very low, 5 = very high).
- The named choices are an initial default; they can be adjusted after the first working version if they do not fit the user's vocabulary.

## History

- Show saved check-ins in reverse chronological order, including the mood, rating, date/time, and note when present.
- Make the history readable on a phone-sized screen as well as a desktop screen.
- Allow the user to delete an individual check-in so an accidental entry can be removed.
- Editing an existing check-in is outside the initial scope; the user can delete an incorrect entry and add it again.

## Interaction and accessibility

- Prioritize quick, touch-friendly controls and a calm, uncluttered layout.
- Use readable text, visible focus states, and labels that do not rely on color alone.
- Handle empty notes normally and avoid saving an entry until the required mood and rating have been selected.
- If saved data cannot be read, show a clear message rather than silently presenting an empty history.

## Out of scope for the initial version

- User accounts, remote storage, cloud backup, and synchronization between browsers or devices.
- Reminders, social sharing, analytics, charts, and exporting/importing data.
- Editing or backdating entries.

## Acceptance criteria

1. The user can save more than one check-in with the same date.
2. Each saved check-in has a named mood, a 1–5 rating, a save-time timestamp, and an optional note.
3. Check-ins remain available after closing and reopening the same browser, provided its site data has not been cleared.
4. The user can review saved check-ins from newest to oldest and delete an individual one.
5. The app clearly explains that data is stored only in the current browser.
6. The page works as a responsive, plain web app without an account or network service.
