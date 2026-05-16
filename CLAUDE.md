# Plot Kalkulátor

## Versioning

The app version is shown in the header (`<p class="version">v1.0.3</p>` in `index.html`).

**Rule: bump the version on every commit that changes user-facing behavior.**

When committing:
1. Increment the version in `index.html` header (`v1.0.3` → `v1.0.4`, etc.). Use semver-ish: patch for fixes/small UI tweaks, minor for new features, major for breaking changes.
2. Update `CACHE` constant in `sw.js` to match (e.g. `'plot-v1.0.4'`) so the service worker invalidates cache and users get the new build.
3. Mention the version in the commit message (e.g. `v1.0.4: ...`).

Skip the bump only for non-shipping changes (CI config, docs, comments).
