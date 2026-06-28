# subnet.

Instant subnet math. No forms. No page reloads. No dependencies.

**[→ Open the calculator](https://bkaganovich.github.io/subnet/)**

---

## What it does

Type anything — a CIDR block, a subnet mask, a hex address, or an IP range — and every value updates immediately. The tool figures out what you typed and responds accordingly.

```
10.0.0.0/22              subnet breakdown — network, broadcast, hosts, mask, wildcard
255.255.252.0            mask → resolves to /22 automatically
/22                      prefix only → shows block size and host count
0xAC100000/20            hex address with optional prefix
10.0.0.0–10.0.3.255      IP range → min enclosing CIDR + exact decomposition
```

---

## Features

**Core calc**
Every field you'd need — network, broadcast, first/last host, mask, wildcard, prefix, usable count. Tap any value to copy it.

**Range → CIDR**
Paste a start–end range and instantly see the minimum enclosing CIDR. If the range isn't CIDR-aligned, the exact decomposition is shown block by block.

**Hex input & display**
Type `0xC0A80100` or `C0A80100` with or without `/cidr`. Toggle the HEX view to see every address in hex beneath the decimal. Switch between `0x` prefix and `no 0x`, `A–F` and `a–f` — handy when matching log formats.

**Binary visualization**
Network bits in cyan, host bits dimmed. The prefix boundary is immediately visible.

**Is this IP in my subnet?**
Type any IP address and get an instant ✓ or ✗ against the current network, plus its offset within the block.

**Subnet splitter**
Enter any subnet and a target prefix. Every resulting block is listed and tappable to copy.

**Route summarizer**
Paste multiple CIDRs (one per line or comma-separated) and get the aggregate route. Flags whether the summary is a perfect match or lossy.

**CIDR scrubber**
Drag the slider to scrub through prefix lengths and watch every value update live.

---

## Shareable links

Every query syncs to the URL. Send a specific calculation to anyone:

```
https://bkaganovich.github.io/subnet/?q=10.0.0.0/22
https://bkaganovich.github.io/subnet/?q=192.168.1.0-192.168.1.254
https://bkaganovich.github.io/subnet/?q=255.255.252.0
```

---

## Works offline

Once loaded, no network required. Bookmark it, pin it, add it to your home screen.

---

## Deploy your own

It's a single HTML file with no build step and no external dependencies beyond a Google Font (which falls back gracefully offline).

```bash
git clone https://github.com/bkaganovich/subnet.git
open index.html
```

To host it yourself, put `index.html` anywhere — any static host, S3 bucket, Nginx, or GitHub Pages will serve it.

---

## Built for

Network engineers who need answers immediately — not after filling out a form.
