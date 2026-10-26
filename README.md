# From eMule MP3s to the Decentralized Web: The Crazy History of Peer-to-Peer

A 45-minute conference talk deck built with **[Reveal.js](https://github.com/hakimel/reveal.js/)** using external Markdown slides ([`slides.md`](./slides.md)) and a custom retro Y2K / Winamp / eMule cyber theme ([`css/theme-y2k.css`](./css/theme-y2k.css)).

---

## Quick Start

Because Reveal.js fetches [`slides.md`](./slides.md) dynamically via `fetch()`, serve the directory over a local HTTP server:

```bash
# Option 1: Using Python 3 (built-in on macOS/Linux)
python3 -m http.server 8000

# Option 2: Using Node.js npx
npx serve -l 8000
```

Then open **[http://localhost:8000](http://localhost:8000)** in your browser.

---

## Presenter Shortcuts

| Key | Action |
| :--- | :--- |
| <kbd>Space</kbd> | Next slide (follows vertical deep-dives, then moves horizontally to the next act) |
| <kbd>←</kbd> <kbd>→</kbd> | Navigate horizontally between **Acts** |
| <kbd>↑</kbd> <kbd>↓</kbd> | Navigate vertically through **Deep-Dive Slides** within an Act |
| <kbd>S</kbd> | Open **Speaker Notes Window** (with timer, upcoming slide preview, and timestamped talk track) |
| <kbd>O</kbd> or <kbd>Esc</kbd> | Toggle **2D Slide Overview Grid** |
| <kbd>F</kbd> | Toggle **Fullscreen Mode** |
| <kbd>C</kbd> | Toggle **CRT Scanline Overlay** on/off (also clickable in top-right status bar) |

---

## Talk Structure (39 Slides / 45 Minutes)

- **Act 0: Cold Open — The 2003 Bedroom Experience (00:00 – 06:45)**
  - Title & eMule 99.9% status bar
  - 4:30 PM after-school ADSL ritual
  - Russian roulette of Kazaa/LimeWire filenames (`Linkin_Park.mp3.exe`)
  - Stuck at 99.9% & `.part` file archaeology in VLC
  - Why P2P was the largest adversarial distributed systems lab in history
  - Talk roadmap
- **Act I: Gen 1 — Napster & The Central Index Fallacy (06:45 – 12:45)**
  - Before Napster: HTTP/FTP client-server bottlenecks
  - Shawn Fanning & Dorm Room 300 (June 1999)
  - Napster Hybrid P2P Architecture (`O(1)` central index + direct TCP transfer)
  - The University Campus Bandwidth Crisis (75% of T3 pipes)
  - Metallica's 13 boxes of paper & *A&M Records v. Napster* ("One throat to choke")
- **Act II: Gen 2 — Cut Off One Head: Gnutella, Kazaa & eMule (12:45 – 22:30)**
  - Justin Frankel's 24-hour renegade release of Gnutella (March 2000)
  - Unstructured Query Flooding & the $O(b^{\text{TTL}})$ meltdown
  - FastTrack & Kazaa's self-organizing Supernode hierarchy (and how it became **Skype**)
  - eDonkey2000 & "Merkur" creating open-source **eMule** (`ed2k://` + 9.28 MB chunk hashing)
  - The trauma of **High ID vs. Low ID** (NAT port forwarding `4662` TCP / `4672` UDP)
  - The Dirty War: Overpeer/MediaDefender poisoning, RIAA lawsuits, Razorback 2.0 raid
  - How eMule fought back: AICH SHA-1 Merkle trees & 384-bit RSA credit signatures
- **Act III: Gen 3 — BitTorrent, Kademlia & Mathematical Invincibility (22:30 – 31:30)**
  - Why eMule struggled with Flash Crowds vs. Bram Cohen's **BitTorrent** (2001)
  - Piece Selection: *Random First*, *Rarest First*, and *Endgame Mode*
  - Game Theory in Code: *Tit-for-Tat* choking & *Optimistic Unchoking*
  - The Culture of the Ratio: Private trackers, Seedboxes, *OiNK's Pink Palace* & *What.cd*
  - The Tracker Achilles' heel
  - **Kademlia DHT** (Maymounkov & Mazières, 2002) & the **XOR Metric** ($d(x,y) = x \oplus y$)
  - $O(\log N)$ routing across 10M+ nodes & trackerless **Magnet Links**
- **Act IV: Plot Twist — P2P Under the Hood of Modern Infra (31:30 – 37:15)**
  - How µTorrent's creator (Ludvig Strigeus) built **Spotify's** desktop P2P streaming engine (88.4% bandwidth offloaded!)
  - Windows 10/11 Delivery Optimization, Blizzard's WoW Downloader & **Uber Kraken / CNCF Dragonfly**
  - WebRTC (`STUN`/`TURN`/`ICE`) & **PeerTube** browser-to-browser video swarming
  - Bitcoin's P2P gossip + Sybil resistance & **Mistral AI** dropping 87 GB LLMs via Magnet links
- **Act V: The Web of Tomorrow — IPFS, libp2p & Local-First (37:15 – 43:45)**
  - Link Rot (38% of 2013 web gone) & hyperscaler fragility
  - **IPFS** (Juan Benet, 2015): Kademlia + Bitswap + Git Merkle DAGs
  - Location Addressing (`https://`) vs. Content Addressing (`ipfs://bafy...` CIDs)
  - **libp2p**, **Iroh**, **Syncthing**, and Local-First software
  - 25-Year Comparison Matrix (Gen 1 → Gen 4)
- **Finale: Don't Just Leech — Keep Seeding! (43:45 – 45:00)**
  - 3 Engineering Takeaways + Seminal Papers & Open-Source Toolkits
