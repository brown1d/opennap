# Original Napster client web snapshots

These are offline adaptations of Napster's own Internet Archive captures.
The table below links to each original. The local HTML keeps the historical
text and table layout. Recovered images are under `assets/` and retain
their original host and path. The October Home snapshot serves the captured
URL with `?02b103`. The June Home snapshot has its own filename so it can
be compared side by side.

| Local path | Original snapshot |
| --- | --- |
| `client/home.html?02b103` | [October 12, 2001](https://web.archive.org/web/20011012195730/http://www.napster.com:80/client/home.html?02b103) |
| `client/home-june-2001.html` | [June 13, 2001](https://web.archive.org/web/20010613232912/http://www.napster.com:80/client/home.html) |
| `client/discover.html` | [August 1, 2001](https://web.archive.org/web/20010801155810/http://www.napster.com:80/client/discover.html) |
| `client/help/` | [June 13, 2001](https://web.archive.org/web/20010613155646/http://www.napster.com:80/client/help/) |
| `client/upgrade.html` | [December 13, 2001](https://web.archive.org/web/20011213221159/http://www.napster.com/client/upgrade.html) |

The samples preserve links between included pages. Scripts, automatic
refresh, submissions, and links to external or uncaptured destinations are
disabled for offline browsing. In particular, the archived Upgrade page
does not launch an update. Missing image labels or transparent spacers
identify or preserve the position of artwork that could not be retrieved.
The bundle includes 52 archived images and the original stylesheet.
The 52 image URLs that could not be retrieved are listed in
`missing-assets.txt`. That list records gaps in this bundle, even where
Wayback may have a capture.

Open `index.html` to browse the samples. If `docs/html` is already being
served, visit `/classic/` to preview. To use these captures for the embedded
client's `/client/...` requests, point the legacy HTTP virtual host's
document root at `docs/html/classic`. The OpenNap replacement pages remain
available from the parent document root.
