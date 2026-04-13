# Patchnotes

## Latest Public Sync

This update is a big cleanup and feature sync for Jane's public repo. It is not every tiny commit, because nobody needs a thirty-page scroll of bot entrails. This is the broad version.

## Added

- Added new setup docs for getting Jane running on a fresh machine.
- Added runbooks for the bigger systems that needed a map, including sessions, server recovery, Best Of, training log mirroring, and auto Git updates.
- Added public-safe dependency tracking through `requirements.txt`.
- Added organization profile support so Jane can handle different guild setups more cleanly.
- Added training log mirroring, including backfill support and tidier archive messages.
- Added broader training stats support using mirrored and stored training result logs.
- Added more flexible background-check review routing for adult and minor queues.
- Added more help text for slash commands, hidden commands, text commands, gambling, training stats, and utility features.

## Created

- Created a better documentation structure under `docs/`.
- Created feature-specific docs for systems that are easy to break if nobody remembers how they work.
- Created file notes for important support files like SQLite, training logs, recruitment sheets, and server safety.
- Created public-safe config examples and setup guidance for new devs.

## Improved

- Improved training log parsing so Jane recognizes more event result formats.
- Improved training log backfills so one weird old message does not stop the whole scan.
- Improved mirrored training log messages so they avoid unnecessary pings.
- Improved organization-aware behavior for role checks, channels, queues, curfew, and stats.
- Improved suggestion handling by simplifying the current flow and removing older external-task behavior.
- Improved docs around deployment, operations, architecture, features, and local setup.

## Fixed

- Fixed several training log edge cases where extra control lines could be treated like attendees.
- Fixed some background-check role and queue permission behavior.
- Fixed channel and feature resolution in places that now depend on organization profiles.
- Fixed setup docs that were out of date for the current dependency flow.
- Fixed a handful of smaller command-help and routing issues.

## Removed

- Removed old Freedcamp suggestion-task behavior from the public-safe code path.
- Removed stale docs that pointed new devs at internal-only or one-time workflows.
- Removed unnecessary public exposure of private-only implementation details.

## Notes

The public repo is still intentionally filtered. Some production-only pieces are private, and some docs describe behavior at a high level without exposing the spicy wiring behind it.
