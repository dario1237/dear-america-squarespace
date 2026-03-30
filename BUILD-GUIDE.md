# Squarespace Build Guide — Step by Step
# "Dear America: Your Rights Are on the Line"

---

## BEFORE YOU START — CHECKLIST

- [ ] Squarespace site is open (existing branch-4.org site OR new connected site)
- [ ] You have the PAGE-COPY.md file open for copy-paste
- [ ] You have the CUSTOM-CSS.md file open for the CSS block
- [ ] Montserrat is available as a font choice (it is — Squarespace includes it)
- [ ] You have at least 1 real photo for the hero (or use solid dark color to start)

---

## STEP 1 — COLORS & FONTS (Do this first, once)

1. In the editor, click **Design** (paint bucket icon in left sidebar)
2. Click **Fonts**
   - Set Heading font to: **Montserrat**, weight **Black (900)** or **Bold (700)**
   - Set Body font to: **Source Sans Pro** or **Inter** (both are in Squarespace)
3. Click **Colors**
   - Set your palette to include: `#C41E3A`, `#67BCB8`, `#F4D081`, `#0D0D0D`, `#F8F6F2`
   - These will be available as quick-select colors throughout the builder

---

## STEP 2 — PASTE THE CUSTOM CSS

1. Click **Design** → **Custom CSS**
2. Open CUSTOM-CSS.md and copy everything inside the code block
3. Paste it into the CSS editor
4. Click **Save**
5. You won't see all effects yet — they activate once you add the CSS classes to sections (see Step 3)

---

## STEP 3 — BUILD THE PAGE SECTIONS

Create a new page: **Pages → + (Add Page) → Blank Page**
Name it: `Dear America` | Slug: `dear-america`

Then build each section in order. For each section:
- Add a new **Section** (click + between sections)
- Choose the layout type listed below
- Copy-paste the text from PAGE-COPY.md
- Add the CSS class (Section gear icon → Advanced → Section CSS Class)

---

### SECTION ORDER & TYPES

| # | Section | Squarespace Layout Type | CSS Class |
|---|---|---|---|
| — | Announcement Bar | Design → Announcement Bar | (built-in) |
| 1 | Hero | **Banner** or **Cover Page** | `hero-section` |
| 2 | Crisis Band | **Single full-width text block** | `crisis-band` |
| 3 | Narrative Cards | **3-column layout** with Text blocks | `narrative-cards` |
| 4 | The Letters | **Blog section** (Grid display) | `letters-section` |
| 5 | Demands | **Text section** with ordered list | `demands-section` |
| 6 | Voices | **Team/Profile grid** or Image+Text cards | `voices-section` |
| 7 | Form | **Form block** | `form-section` |
| 8 | What's at Stake | **6-column or 2×3 grid** text blocks | `stakes-section` |
| 9 | Take Action | **3-column layout** | `action-section` |
| 10 | Footer | Standard Squarespace Footer | (built-in) |

---

## STEP 4 — SET UP THE LETTERS BLOG

The letters grid uses Squarespace's built-in Blog feature.

1. Go to **Pages → Not Linked → + → Blog**
2. Name it: `Letters`
3. Go to the Letters blog settings:
   - Display: **Grid** (2 or 3 columns)
   - Show: Excerpt, Category, Title, Read More button
   - Hide: Author, Date (for anonymity — unless you want to show it)
4. Create **Categories** (these become the filter tags):
   - HUD Worker
   - Former Federal Employee
   - Elected Official
   - Community Leader
   - Civil Rights Organization
   - Faith Leader
5. Add the 6 placeholder letter posts from PAGE-COPY.md
6. Embed the blog grid into your main page using a **Summary Block** pointed at the Letters blog

**To add a filter above the grid:**
Use a **Code Block** with this simple HTML filter (paste above the Summary Block):

```html
<div class="letter-filters">
  <a href="?category=all">All</a>
  <a href="?category=hud-worker">HUD Workers</a>
  <a href="?category=former-federal-employee">Former Feds</a>
  <a href="?category=elected-official">Electeds</a>
  <a href="?category=community-leader">Community</a>
  <a href="?category=civil-rights-organization">Civil Rights Orgs</a>
  <a href="?category=faith-leader">Faith Leaders</a>
</div>
<style>
.letter-filters {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-bottom: 30px;
}
.letter-filters a {
  background: #F8F6F2;
  border: 1.5px solid #67BCB8;
  color: #1A1A1A;
  padding: 8px 18px;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  text-decoration: none;
  transition: all 0.2s;
}
.letter-filters a:hover {
  background: #67BCB8;
  color: white;
}
</style>
```

---

## STEP 5 — LANGUAGE DUPLICATE

When ready to add Spanish (or other language):

1. In Pages panel, right-click the `Dear America` page
2. Click **Duplicate**
3. Rename it: `Estimada América` | Slug: `dear-america-es`
4. Open the duplicate and translate all text blocks
5. In the navigation, add a small text block or button pair in the header:
   - `EN` → links to `/dear-america`
   - `ES` → links to `/dear-america-es`
6. Apply CSS class `lang-switch` to that nav element
7. Repeat for additional languages as needed

---

## STEP 6 — NAVIGATION

Add the page to the site nav:
- Main nav: `Dear America` or just `Letters`
- Make sure the `SHARE YOUR STORY` button in the hero and Take Action section links down the same page using anchor links (Squarespace supports anchor links via section IDs)

To set anchor links:
1. On the form section, click the gear icon → Advanced → **Section ID** → type: `share-your-story`
2. On the letters section: **Section ID** → type: `letters`
3. Hero button 1 links to: `#letters`
4. Hero button 2 links to: `#share-your-story`

---

## PLACEHOLDER NOTES
When your friend sends the real content, replace these:

| Placeholder | Replace with |
|---|---|
| `[PHOTO PLACEHOLDER]` | Headshot or photo of the voice/surrogate |
| `[NAME]` | Full name (or "Anonymous") |
| `[TITLE / AFFILIATION]` | Their role and org |
| `[PULL QUOTE]` | 1–2 sentence excerpt from their letter |
| `[EMAIL ADDRESS]` | The campaign's secure contact email |
| Placeholder letter cards 1–6 | Real letters as they come in |

---

## QUICK REFERENCE — KEY COLORS

| Use | Hex |
|---|---|
| Crimson (primary action) | `#C41E3A` |
| Teal (secondary action) | `#67BCB8` |
| Gold (accent/numbers) | `#F4D081` |
| Near-black (dark sections) | `#0D0D0D` |
| Cream (light sections) | `#F8F6F2` |
| Body text | `#1A1A1A` |
