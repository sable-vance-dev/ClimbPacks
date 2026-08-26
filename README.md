# ClimbPacks

Offline state packs for [OpenClimb](https://github.com/sable-vance-dev/OpenClimb).
The app fetches `releases/latest/download/manifest.json` and downloads the
`.pack` archives it names — this repository exists to host those releases, and
its git history is deliberately just this notice.

## Data licence

Route data comes from [OpenBeta](https://openbeta.io) under
[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). The packs are
a derived work — the same data reorganized for offline use, not rewritten —
published under the same licence. Every release carries the full attribution
in its notes; redistribution without it is not permitted.

## How releases are built

`scripts/build-all-packs.sh` and `scripts/publish-packs.sh` in the OpenClimb
repository, quarterly via its `harvest` workflow or by hand. Each release is
one immutable pack set under one tag; the manifest's checksums are what every
device verifies before installing.
