# Custom CSS for Squarespace
# How to add: Design → Custom CSS → paste the entire block below

---

## WHERE TO PASTE THIS
1. In Squarespace editor: click **Design** (paint bucket icon)
2. Click **Custom CSS**
3. Paste everything in the code block below
4. Click **Save**

---

```css
/* ============================================
   DEAR AMERICA CAMPAIGN — SQUARESPACE CSS
   Primary: branch-4.org style
   Secondary: federalunionists.net style
   ============================================ */

/* --- GLOBAL VARIABLES --- */
:root {
  --crimson: #C41E3A;
  --teal: #67BCB8;
  --gold: #F4D081;
  --dark: #0D0D0D;
  --cream: #F8F6F2;
  --white: #FFFFFF;
  --body-text: #1A1A1A;
}

/* --- GLOBAL FONT OVERRIDE --- */
/* Only applies if Montserrat is selected as the heading font in Design → Fonts */
h1, h2, h3, h4 {
  letter-spacing: -0.02em;
  line-height: 1.1;
}

/* --- ANNOUNCEMENT BAR --- */
.sqs-announcement-bar {
  background-color: var(--crimson) !important;
  color: var(--white) !important;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  font-size: 13px;
}

/* --- HERO SECTION --- */
/* Target your hero section by adding the CSS class "hero-section" in the section settings */
.hero-section {
  background-color: var(--dark);
}

.hero-section h1 {
  color: var(--white);
  font-size: clamp(2.5rem, 6vw, 5rem);
  font-weight: 900;
  text-transform: uppercase;
  line-height: 1.05;
}

.hero-section p {
  color: var(--crimson);
  font-size: clamp(1.1rem, 2vw, 1.4rem);
  font-weight: 600;
}

/* Hero primary button */
.hero-section .sqs-block-button-element--large,
.hero-section .sqs-button-element--primary {
  background-color: var(--crimson) !important;
  color: var(--white) !important;
  border: none;
  border-radius: 0;
  font-weight: 800;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 16px 36px;
  transition: background-color 0.2s ease;
}

.hero-section .sqs-block-button-element--large:hover {
  background-color: #a01830 !important;
}

/* Hero secondary button */
.hero-section .sqs-button-element--secondary {
  background-color: transparent !important;
  color: var(--teal) !important;
  border: 2px solid var(--teal) !important;
  border-radius: 0;
  font-weight: 800;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 14px 34px;
  transition: all 0.2s ease;
}

.hero-section .sqs-button-element--secondary:hover {
  background-color: var(--teal) !important;
  color: var(--dark) !important;
}

/* --- CRISIS BAND --- */
/* Add CSS class "crisis-band" to this section */
.crisis-band {
  background-color: var(--crimson) !important;
}

.crisis-band p,
.crisis-band blockquote {
  color: var(--white);
  font-size: clamp(1.2rem, 2.5vw, 1.8rem);
  font-weight: 700;
  text-align: center;
  line-height: 1.5;
  max-width: 900px;
  margin: 0 auto;
}

/* --- NARRATIVE CARDS (3-column) --- */
/* Add CSS class "narrative-cards" to this section */
.narrative-cards {
  background-color: var(--cream) !important;
}

.narrative-cards .sqs-block-summary-v2-item,
.narrative-cards .sqs-col {
  border-top: 4px solid var(--teal);
  padding-top: 20px;
}

.narrative-cards h3 {
  color: var(--body-text);
  font-weight: 800;
  font-size: 1.1rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  margin-bottom: 12px;
}

.narrative-cards p {
  color: #444;
  line-height: 1.7;
}

/* --- LETTERS SECTION --- */
/* Add CSS class "letters-section" to this section */
.letters-section {
  background-color: var(--white);
}

.letters-section h2 {
  color: var(--body-text);
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 900;
}

/* Blog grid card styling */
.letters-section .BlogList-item,
.letters-section article {
  border: none;
  border-top: 3px solid var(--crimson);
  padding: 24px 0;
  transition: transform 0.2s ease;
}

.letters-section .BlogList-item:hover {
  transform: translateY(-4px);
}

/* Tags/category labels on letter cards */
.letters-section .BlogList-item-category,
.letters-section .category-label {
  background-color: var(--teal);
  color: var(--white);
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 4px 10px;
  display: inline-block;
  margin-bottom: 12px;
}

/* Read more link on cards */
.letters-section .BlogList-item-readmore,
.letters-section a.read-more {
  color: var(--teal);
  font-weight: 700;
  text-transform: uppercase;
  font-size: 13px;
  letter-spacing: 0.08em;
  text-decoration: none;
  border-bottom: 2px solid var(--teal);
}

/* --- DEMANDS SECTION --- */
/* Add CSS class "demands-section" to this section */
.demands-section {
  background-color: var(--dark) !important;
}

.demands-section h2 {
  color: var(--white);
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 900;
  margin-bottom: 40px;
}

/* Numbered list with gold numbers */
.demands-section ol {
  list-style: none;
  counter-reset: demands-counter;
  padding: 0;
  max-width: 750px;
  margin: 0 auto;
}

.demands-section ol li {
  counter-increment: demands-counter;
  color: var(--white);
  font-size: clamp(1rem, 2vw, 1.3rem);
  font-weight: 600;
  padding: 18px 0 18px 60px;
  border-bottom: 1px solid rgba(255,255,255,0.1);
  position: relative;
  line-height: 1.4;
}

.demands-section ol li::before {
  content: counter(demands-counter);
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  color: var(--gold);
  font-weight: 900;
  font-size: 2rem;
  line-height: 1;
}

/* --- VOICES SECTION --- */
/* Add CSS class "voices-section" to this section */
.voices-section {
  background-color: var(--cream) !important;
}

.voices-section h2 {
  color: var(--body-text);
  font-weight: 900;
}

/* Profile/team card styles */
.voices-section .sqs-block-image,
.voices-section .profile-card-image {
  border-radius: 0;
  filter: grayscale(20%);
}

/* Pull quote style on voice cards */
.voices-section blockquote,
.voices-section .pull-quote {
  border-left: 4px solid var(--teal);
  padding-left: 16px;
  color: #444;
  font-style: italic;
  font-size: 1rem;
  line-height: 1.6;
}

/* --- FORM SECTION --- */
/* Add CSS class "form-section" to this section */
.form-section {
  background-color: var(--crimson) !important;
}

.form-section h2 {
  color: var(--white);
  font-size: clamp(2rem, 4vw, 3.5rem);
  font-weight: 900;
}

.form-section p {
  color: rgba(255,255,255,0.9);
  font-size: 1.1rem;
  line-height: 1.7;
}

/* Form fields */
.form-section .field-element,
.form-section input,
.form-section textarea,
.form-section select {
  background-color: rgba(255,255,255,0.12) !important;
  border: 1.5px solid rgba(255,255,255,0.4) !important;
  color: var(--white) !important;
  border-radius: 0;
  padding: 14px 16px;
}

.form-section input::placeholder,
.form-section textarea::placeholder {
  color: rgba(255,255,255,0.6);
}

/* Form submit button */
.form-section .form-button-wrapper button,
.form-section input[type="submit"] {
  background-color: var(--dark) !important;
  color: var(--white) !important;
  border: none;
  border-radius: 0;
  font-weight: 800;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 16px 40px;
  font-size: 14px;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.form-section input[type="submit"]:hover {
  background-color: #222 !important;
}

/* --- WHAT'S AT STAKE TILES --- */
/* Add CSS class "stakes-section" to this section */
.stakes-section {
  background-color: var(--white);
}

.stakes-section h2 {
  color: var(--body-text);
  font-weight: 900;
}

.stakes-section .sqs-col,
.stakes-section .tile {
  padding: 28px;
  border-top: 4px solid var(--crimson);
  transition: border-color 0.2s ease;
}

.stakes-section .sqs-col:hover,
.stakes-section .tile:hover {
  border-top-color: var(--teal);
}

.stakes-section h3 {
  font-weight: 800;
  font-size: 1rem;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  color: var(--body-text);
  margin-bottom: 10px;
}

.stakes-section p {
  font-size: 0.95rem;
  color: #555;
  line-height: 1.7;
}

/* --- TAKE ACTION SECTION --- */
/* Add CSS class "action-section" to this section */
.action-section {
  background-color: var(--dark) !important;
}

.action-section h2 {
  color: var(--white);
  font-weight: 900;
}

.action-section h3 {
  color: var(--teal);
  font-weight: 800;
  font-size: 1.1rem;
  text-transform: uppercase;
  letter-spacing: 0.06em;
}

.action-section p {
  color: rgba(255,255,255,0.8);
  line-height: 1.7;
}

.action-section .sqs-block-button-element {
  background-color: var(--crimson) !important;
  color: var(--white) !important;
  border: none;
  border-radius: 0;
  font-weight: 800;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 14px 28px;
}

/* --- FOOTER --- */
footer .sqs-block-content,
.Footer-inner {
  border-top: 4px solid var(--crimson);
}

footer p,
.Footer-inner p {
  font-size: 12px;
  color: #888;
  line-height: 1.6;
}

/* --- GLOBAL BUTTON OVERRIDES --- */
/* Makes all buttons sharp-edged (no rounded corners) to match both reference sites */
.sqs-block-button-element,
.sqs-button-element--primary,
.sqs-button-element--secondary {
  border-radius: 0 !important;
}

/* --- ANIMATED UNDERLINE (FUN style) --- */
/* Add class "animated-underline" to any text block to get this effect */
.animated-underline span {
  background-image: linear-gradient(var(--teal), var(--teal));
  background-repeat: no-repeat;
  background-position: 0 95%;
  background-size: 0% 3px;
  transition: background-size 0.4s ease;
}

.animated-underline:hover span {
  background-size: 100% 3px;
}

/* --- LANGUAGE SWITCHER NAV BUTTONS --- */
/* Style for language toggle buttons added to the nav */
.lang-switch {
  display: inline-flex;
  gap: 8px;
  align-items: center;
}

.lang-switch a {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.08em;
  padding: 5px 10px;
  border: 1.5px solid currentColor;
  text-decoration: none;
  transition: all 0.2s ease;
}

.lang-switch a.active {
  background-color: var(--teal);
  color: var(--white);
  border-color: var(--teal);
}

/* --- MOBILE RESPONSIVE ADJUSTMENTS --- */
@media (max-width: 767px) {
  .demands-section ol li {
    padding-left: 50px;
    font-size: 1rem;
  }

  .demands-section ol li::before {
    font-size: 1.5rem;
  }

  .hero-section h1 {
    font-size: 2.4rem;
  }

  .form-section h2 {
    font-size: 2rem;
  }
}
```

---

## HOW TO APPLY SECTION CSS CLASSES IN SQUARESPACE

For each section, you need to add the CSS class name so the styles above work:

1. Click the section you want to style
2. Click the **gear icon** (Section Settings)
3. Go to **Advanced**
4. In the **Section CSS Class** field, type the class name (no dot)

| Section | CSS Class to add |
|---|---|
| Hero | `hero-section` |
| Crisis Band | `crisis-band` |
| Narrative Cards | `narrative-cards` |
| Letters Grid | `letters-section` |
| Demands | `demands-section` |
| Voices | `voices-section` |
| Form | `form-section` |
| What's at Stake | `stakes-section` |
| Take Action | `action-section` |
