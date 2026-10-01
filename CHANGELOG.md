# Changelog

All notable changes to this repository are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added

- Organisation profile, default community files and templates that send issues and pull requests to the monorepo.

### Changed

- The organisation profile is rewritten as a full front page: a centred logo with quick links, why PHAEMOS exists, the meaning behind the name, a diagram of how the nodes, gateway, API and dashboard connect, what it does, where it stands with the four milestones, a stack table, the repositories and every way to get involved.
- The organisation profile adds a roadmap table linking the four milestones, a tech stack line and the CERN-OHL-S hardware licence. Get involved now starts with the welcome and roadmap discussions.
- `README.md` names AGPL-3.0-or-later and points to the monorepo `NOTICE.md` for the hardware licence.
- The organisation profile opens with the PHAEMOS logo, which switches between its light and dark versions with the viewer's theme. A note gives the current phase and a Get involved section lists every way in.
- Links to phaemos.com, the status page and the documentation site are gone from the profile, `SUPPORT.md` and the new issue page, since those sites go live with the Launch milestone. The new issue page links the roadmap board instead.

### Fixed

- `CODE_OF_CONDUCT.md` linked a contact page on phaemos.com, which is not live yet. Reports now go to the contact address alone.
