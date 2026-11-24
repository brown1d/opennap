# Napster client pages

Serve this directory as the document root for the legacy client's local HTTP
site. Home, Discover, and Help are original, period-inspired replacements
with local GIF graphics. The pages use HTML 4.01 Transitional, tables, basic
CSS, and ASCII text with a Windows-1252 declaration. They require no scripts,
plugins, external images, or services.

## Request mapping

| Request from the Windows client | File |
| --- | --- |
| `/client/home.html?02b103` | `client/home.html` |
| `/client/discover.html` | `client/discover.html` |
| `/client/help/` | `client/help/index.html` |
| `/client/help` | Standard directory redirect to `/client/help/` |

Serve the files over plain HTTP on port 80 with `index.html` enabled as a
directory index. The Home query string is handled by normal static file
serving. The server should return `text/html`, `text/css`, and `image/gif`
for the corresponding files. Keep redirects on the local HTTP origin.

To preview on the machine hosting OpenNap:

```sh
cd /Users/dbrown/opennap
python3 -m http.server 8080 --bind 127.0.0.1 --directory docs/html
```

Open `http://127.0.0.1:8080/client/home.html?02b103` in a browser on that
machine. For the Windows guest itself, configure a LAN HTTP virtual host
for `www.napster.com` on port 80 with this document root. Map just that web
hostname to the LAN web server in the guest's hosts file or local DNS. Check
for a configured IE proxy if the guest keeps going to the public site. The
Napster metaserver and OpenNap login use separate connections and keep their
existing settings.

## Original snapshots

The new capture shows `www.napster.com` receiving the versioned Home
request, with a modern error body and an HTTPS redirect on separate
requests. Discover and both Help spellings appeared in earlier captures.

The Internet Archive returned these original HTML snapshots:

| Page | Wayback snapshot |
| --- | --- |
| Home with client version query | [October 12, 2001](https://web.archive.org/web/20011012195730/http://www.napster.com:80/client/home.html?02b103) |
| Home without a query | [June 13, 2001](https://web.archive.org/web/20010613232912/http://www.napster.com:80/client/home.html) |
| Discover | [August 1, 2001](https://web.archive.org/web/20010801155810/http://www.napster.com:80/client/discover.html) |
| Help | [June 13, 2001](https://web.archive.org/web/20010613155646/http://www.napster.com:80/client/help/) |

The snapshots are historical documents with absolute URLs to Napster's
image and script hosts, as well as forms and links to separate services.
They are useful for reference. The files served by this directory are
standalone pages for the running legacy client.
