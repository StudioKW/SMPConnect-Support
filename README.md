# SMPConnect-Support

Official issue tracker and support for SMPConnect.

**Find people. Make plans. Play together.**

SMPConnect is a free social activity hub for survival multiplayer servers, published by **KWStudio Gaming**. Players use /connect to discover activities, organize adventures, join other players and read saved activity updates when their community plays at different times.

**Current status: 0.1.0 Beta preparation. The plugin has not been published.** This repository provides support documentation and issue tracking, not download binaries or plugin source. No download link is available yet.

## Activity Hub

- Browse paginated activities and filter Adventure, Building, Mining, Farming and Other.
- Create/edit plans using native Paper dialogs and a confirmation step.
- View participants, join/leave eligible plans and manage activities you created.
- Use My Activities, My Participations and Inbox. Offline activity updates persist until read/dismissed or removed by retention limits.
- Administrators can inspect and cancel inappropriate plans where authorized.

No client mod, resource pack, companion plugin or external database is required. There are no paid features, license keys, telemetry or runtime AI services.

## Supported beta environment

**Minecraft 26.3 / Paper build 249 / Java 25.** Other builds, server implementations and Folia are not advertised as tested.

When an authorized release becomes available: stop Paper, back up the complete plugins/SMPConnect/ data directory and matching JAR, install the official JAR into plugins/, and restart normally. Wait for readiness, then use /connect. Do not use /reload or hot reloaders.

Edit plugins/SMPConnect/config.yml while stopped and restart to apply. Defaults are three active creations per player, 72-hour expiration, maximum capacity 12 including creator, and diagnostic logging off. Ranges: active creations 1–100, expiration 1–8760 whole hours, capacity 2–12.

| Permission | Default | Purpose |
| --- | --- | --- |
| smpconnect.use | true | Menus, participation and Inbox |
| smpconnect.create | true | Create activities within limits; also requires use |
| smpconnect.admin | op | Manage any activity and use console administration; includes use/create |

Creation has a 30-second cooldown. Successful joins/leaves share a five-second player cooldown across activities; it resets on process restart. Schedules use optional ISO UTC text. Inbox keeps the latest 200 updates per recipient, including unread; opening a notice does not mark it read.

## Bugs, ideas and support

- [Report a bug](https://github.com/StudioKW/SMPConnect-Support/issues/new?template=bug_report.yml)
- [Request a feature](https://github.com/StudioKW/SMPConnect-Support/issues/new?template=feature_request.yml)
- [Search existing issues](https://github.com/StudioKW/SMPConnect-Support/issues)
- [Support instructions](SUPPORT.md)
- [Contribution guidance](CONTRIBUTING.md)

Include exact versions, a short description, reproduction steps and expected/actual behavior. Share only short sanitized log excerpts. **Never upload databases, credentials, tokens, private chat, IP addresses, identifying player data or proprietary source.**

For vulnerabilities, use [private security reporting](https://github.com/StudioKW/SMPConnect-Support/security/advisories/new), **never public Issues**. Read [SECURITY.md](SECURITY.md) first.

## Data and limits

Data stays locally in plugins/SMPConnect/activities.sqlite. Back up the entire plugin data directory and matching JAR after Paper has stopped and fully exited. Do not copy only an active database or delete journals. Test upgrades/restoration on a copy; code rollback does not reverse a schema migration. Public support reports do not need your live database.

No Community Projects, matchmaking, friends/guilds, cross-server or Discord features are included. Historical storage has no automatic purge and no general TPS/player-count guarantee is made. Offline names use short UUID labels.

## License and publisher

Published by **KWStudio Gaming**. The intended product license is **free to use, proprietary / All Rights Reserved**, with final legal terms pending approval. Source code remains private; this support repository is not an open-source release or a license grant for the plugin. Third-party components retain their own licenses. No support response time, release date or maintenance period is promised.

Codex generated substantial portions of the implementation, tests and documentation under owner direction and review. The plugin does not use generative AI at runtime. No images, testimonials or usage statistics are claimed here.
