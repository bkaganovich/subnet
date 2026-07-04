# subnet.

Instant subnet math. No forms. No page reloads. No dependencies.

**[→ Open the calculator](https://bkaganovich.github.io/subnet/)**

---

## What it does

Type anything below — a CIDR block, a subnet mask, a hex address, or an IP range — and every value updates immediately. The tool detects the format automatically and shows the right answer.

```
10.0.0.0/22                    subnet breakdown — network, broadcast, hosts, mask, wildcard
192.168.1.0/255.255.255.0      IP + subnet mask → resolves to /24 automatically
255.255.252.0                  mask alone → resolves to /22 automatically
/22                            prefix only → shows block size and host count
0xAC100000/20                  hex address with optional prefix
10.0.0.0–10.0.3.255            IP range → smallest CIDR block that contains it, broken down exactly
```

---

## Features

**Core calculator**
Every field you need — network, broadcast, first/last host, mask, wildcard, prefix, usable count. Tap any value to copy it.

**Range → CIDR**
Paste a start and end IP address to see the smallest CIDR block that contains the whole range. If the range does not match a CIDR block exactly, you will also see it broken down into exact pieces.

**Hex input & display**
Type `0xC0A80100` or `C0A80100`, with or without `/cidr`. Toggle the HEX view to see every address in hex below the decimal version. You can switch between `0x` prefix and no prefix, and between `A–F` and `a–f` — useful when comparing against log files.

**Binary visualization**
Network bits are shown in cyan, host bits are dimmed, so you can instantly see where the prefix boundary falls.

**Is this IP in my subnet?**
Type any IP address to get an instant ✓ or ✗ against the current network, plus how far it sits from the start of the block.

**Subnet splitter**
Enter a subnet and a target prefix. Every resulting block is listed, and you can tap any block to copy it.

**Route summarizer**
Paste multiple CIDRs (one per line, or separated by commas) to get one CIDR that covers all of them. It tells you if that summary is an exact match or if it includes extra addresses.

**CIDR scrubber**
Drag the slider to try different prefix lengths and watch every value update live.

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

It is a single HTML file — no build tools, no installs. It uses one Google Font, but still works fine without internet.

```bash
git clone https://github.com/bkaganovich/subnet.git
open index.html
```

To host it yourself, put `index.html` anywhere — any static host, S3 bucket, Nginx, or GitHub Pages will serve it.

---

## Built for

Network engineers who need answers immediately — not after filling out a form.
