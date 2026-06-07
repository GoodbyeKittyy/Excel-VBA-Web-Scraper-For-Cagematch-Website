# Web Scraper For CageMatch Website

Hi there! Thank you for stopping by 🙂

This project is a fully functional Excel Macro-Enabled workbook that scrapes match data from [CageMatch](https://www.cagematch.net), an online professional wrestling database.

> 🚀 **New Python version available!** If you've starred this project, you may want to check out the [improved Python rewrite](https://github.com/GoodbyeKittyy/Python-Web-Scraper-For-Cagematch-Website) — it features a full GUI, multi-promotion scraping, WON/Meltzer star support, stealth browser automation, and Excel export with richer formatting. The original Excel VBA version is still here and fully functional.

---

## Background

I'm a big professional wrestling fan and built this tool because every wrestling match database — including CageMatch — lacks a sort function. You have to click through dozens of individual links just to find the highest-rated matches. As of 2024, that still hasn't changed, so I built this to do it automatically.

---

## How to Use

**1. Copy the matchguide URL you want to scrape.**

For example: `https://www.cagematch.net/?id=8&nr=1&page=7`

![Step 1](https://github.com/GoodbyeKittyy/Web-Scraper-For-Cagematch-Website/assets/161730857/35d03fea-7212-47d9-94e4-0f83c9af4689)

---

**2. Paste the link into cell B2 and press the "Extract Web Data" button.**

![Step 2](https://github.com/GoodbyeKittyy/Web-Scraper-For-Cagematch-Website/assets/161730857/f4f9e92c-6753-425f-b3d9-1a8b18a8403e)

---

**3. Wait for it to finish.**

The macro will page through every entry in the list and pull detailed info (match type, event name) for every match rated **8.00 or above**. Larger lists will take a few minutes.

Extracted columns:

| Column | Description |
|--------|-------------|
| Date | Match date |
| Match Fixture | Hyperlink to the match page |
| Match Type | e.g. Singles, Tag Team |
| Event | Event name |
| WON | Won/loss result |
| Rating | Community rating |
| Votes | Number of votes |

---

**4. Results are color-coded by rating.**

| Color | Condition |
|-------|-----------|
| ⬛ Black fill, 🟡 Gold font | Rating ≥ 9.5 |
| 🟡 Gold fill, ⬛ Black font | Rating ≥ 8.5 and < 9.5 |
| 🔵 Blue fill, ⬛ Black font | Rating ≥ 8.0 and < 8.5 |

![Step 3](https://github.com/GoodbyeKittyy/Web-Scraper-For-Cagematch-Website/assets/161730857/dc053e55-3181-4522-803d-e5fdcda8574c)

---

## Requirements

- Microsoft Excel with macros enabled
- Windows (uses `XMLHTTP60` and `MSHTML` — Excel for Windows only)
- An internet connection

---

## Limitations

- Scrapes **one promotion at a time** — you paste a single URL manually
- No WON/Meltzer star rating support
- No date filtering
- Stops as soon as it hits a match rated below 8.0 (early exit)
- Can be blocked by CageMatch if requests are sent too quickly

If any of these are a pain point, the [Python version](https://github.com/GoodbyeKittyy/Python-Web-Scraper-For-Cagematch-Website) addresses all of them.
