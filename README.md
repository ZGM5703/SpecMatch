# 💻 SpecMatch — Laptop Comparison Tool

An interactive, browser-based laptop spec comparator built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies, no setup required. Compare up to 3 laptops side by side with automatic winner highlighting per spec category.

**🔗 Live demo:** `https://ZGM5703.github.io/laptop-comparator/` *(after enabling GitHub Pages — see below)*

---

## What it does

You select up to **3 laptops** from a dataset of 18 real models across ASUS, Lenovo, Acer, MSI, HP, and Dell. SpecMatch then builds a side-by-side comparison table that automatically highlights the **winner in each spec row** — so you can instantly see which laptop leads in performance, display quality, battery life, weight, and price.

---

## How to run it

**Option 1 — Live demo:** Open the GitHub Pages link above directly in any browser.

**Option 2 — Run locally:**
1. Download or clone this repository
2. Open `index.html` in any modern browser
3. That's it — no install, no build step

```bash
git clone https://github.com/ZGM5703/laptop-comparator.git
cd laptop-comparator
open index.html
```

---

## Features

- **18 real laptop models** — ASUS, Lenovo, Acer, MSI, HP, Dell with accurate specs and PH market prices
- **Brand filter per slot** — narrow each dropdown to a specific brand before selecting
- **Conflict prevention** — a laptop selected in one slot is automatically disabled in all others
- **Auto winner highlighting** — green cells mark the best spec value per row; amber marks the lowest price
- **Smooth scroll to results** — table scrolls into view automatically after clicking Compare
- **Clear per slot** — remove one laptop without resetting the others
- **Responsive layout** — slots stack on mobile

---

## How the comparison works

1. **Select a laptop** in each of the 3 slots using the brand filter and dropdown
2. Click **Compare Laptops** — the button activates once 2 or more slots are filled
3. The app builds a spec table grouped into sections: Performance, Storage, Display, Portability, and Price
4. For each spec row, the app reads a numeric score value for each laptop:
   - For most specs (CPU, GPU, RAM, display, battery) — **higher score wins**, highlighted green
   - For weight and price — **lower value wins**, highlighted amber
   - If all selected laptops score equally on a spec, no winner is highlighted
5. Prices shown are **mid-2025 Philippine market estimates** — always verify with your retailer before buying

---

## Laptop dataset

| Brand   | Models included |
|---------|----------------|
| ASUS    | VivoBook 15 OLED, ZenBook 14 OLED, TUF Gaming A15, ROG Strix G16 |
| Lenovo  | IdeaPad Slim 5, ThinkPad E14, Legion 5, Yoga Slim 7 Pro |
| Acer    | Aspire 5, Swift Go 14, Nitro V 15 |
| MSI     | Modern 14, Katana 15, Creator M16 |
| HP      | Pavilion 15, Envy x360 14 |
| Dell    | Inspiron 15, XPS 13 |

---

## Technologies used

- HTML5
- CSS3 (CSS variables, CSS Grid, dynamic inline styles)
- Vanilla JavaScript (no libraries or frameworks)
- Dynamic DOM generation — the comparison table is fully built in JavaScript from a structured data array

---

## What I learned

- Structuring a real-world dataset as a JavaScript object array and deriving UI from it dynamically
- Building a dynamic CSS Grid layout where the number of columns changes based on user selections
- Implementing conflict prevention logic — disabling already-selected options across multiple dropdowns
- Writing a winner-detection algorithm that compares numeric scores and handles ties gracefully
- Separating display values from comparison scores (e.g. showing "16GB DDR5" while scoring `16` for comparison)

---

## How a production version would work

This portfolio version uses a hardcoded dataset. A production version would:

- Pull live product data and prices from a retailer API (e.g. Lazada, Shopee, or a price comparison service)
- Store the dataset in a backend database with regular price update jobs
- Add user-submitted reviews and verified purchase data
- Support filtering by price range, use case (gaming, office, student), and screen size

---

## Future improvements

- [ ] Add more laptop models and keep prices updated
- [ ] Filter laptops by use case (gaming, student, business, creative)
- [ ] Price range slider to narrow the selection
- [ ] "Best for your budget" recommendation based on overall score
- [ ] Share comparison via URL

---

## License

MIT — free to use, modify, and share.
