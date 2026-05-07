# Mother's Day Timeline of Us — Implementation Plan

> **For Hermes:** Single-file HTML/CSS/JS implementation. No build tools needed.

**Goal:** Build a beautiful, animated "Timeline of Us" Mother's Day website that scrolls through your family's most cherished moments with her.

**Architecture:** Single self-contained HTML file with inline CSS and JavaScript. No external dependencies except Google Fonts. Uses CSS animations, Intersection Observer for scroll-triggered reveals, and a warm romantic aesthetic.

**Tech Stack:** Vanilla HTML5, CSS3, JavaScript (ES6+) — no frameworks, no build step.

---

## Files to Create

- `mothers-day-timeline/index.html` — the complete single-file website

---

## Design Specifications

### Color Palette
- Background: Warm cream `#faf6f1`
- Accent: Soft rose `#d4728c`
- Secondary accent: Gold `#c9a87c`
- Text: Deep warm brown `#3d2c2c`
- Secondary text: Warm gray `#7a6565`
- Card background: White `#ffffff` with soft shadow

### Typography
- Google Fonts: 'Playfair Display' (headings, elegant serif) + 'Lora' (body, readable serif)
- Mood: Warm, elegant, editorial — like a beautifully designed photo book

### Layout
- Full-screen hero section with a loving message and floating petal animation
- Vertical timeline with alternating left/right cards on desktop, stacked on mobile
- Each timeline event: photo area (with placeholder), date, title, description
- Smooth scroll-triggered fade-in animations for each card
- Grand finale section with a heartfelt closing message and "open this" CTA

### Animations
- Floating rose petals on the hero section (CSS-only, continuous)
- Cards fade up and slide in as user scrolls (Intersection Observer)
- Subtle parallax on the hero background
- Smooth hover effects on cards

---

## Timeline Event Structure (Sample Events)

Each event has:
- Year (or date)
- Title (short, emotional)
- Description (a paragraph of memory)
- Photo placeholder (user replaces with real photos)

Sample events to include (user will customize):
1. "The Day You Became a Mom" — birth of first child
2. "Our First Family Photo" — early days together
3. "The Day [Child] Was Born" — each child's birth
4. "Our First Vacation" — first family trip
5. "Building Our Home" — settling into family life
6. "Everyday Magic" — the ordinary moments that are extraordinary
7. "How You Make Everything Better" — appreciation card
8. "To the Woman Who Does It All" — final tribute

---

## Implementation Steps

### Step 1: Create project structure

Create `mothers-day-timeline/` directory.

### Step 2: Build the HTML file

The single HTML file will contain:
- `<head>` with Google Fonts, meta tags, all CSS inline
- Hero section: full viewport, gradient background, floating petals, title "Happy Mother's Day, [Her Name]" with subtitle
- Timeline section: vertical line down center, alternating cards
- Each card: photo placeholder (with instructions to replace), date badge, title, description
- Finale section: large heartfelt message with decorative elements
- Footer: "With all our love, [Your Family Names]"

### Step 3: CSS styling
- Responsive design (mobile-first)
- Timeline: CSS pseudo-elements for the vertical line and dot markers
- Card styling: rounded corners, soft shadows, hover lift effect
- Floating petals: multiple absolutely positioned elements with CSS keyframe animations
- Typography hierarchy with Playfair Display and Lora
- Smooth color transitions and fade animations

### Step 4: JavaScript
- Intersection Observer for scroll-triggered fade-in animations
- Smooth scroll behavior
- Optional: gentle parallax on hero section
- All JS inline at bottom of HTML

---

## Customization Guide (for the user after building)

To customize after the build:
1. **Change her name:** Replace `[HER NAME]` with her actual name
2. **Edit timeline events:** Each event in the HTML has a date, title, and description — replace the sample text with your real memories
3. **Add real photos:** Each photo area has a placeholder with a comment like `<!-- REPLACE: Replace background-image URL with your photo -->` — swap in real photo URLs or local paths
4. **Add more events:** Copy the card template HTML and add more entries
5. **Change the final message:** Edit the closing section text
6. **Customize colors:** CSS custom properties at the top of the `<style>` block

---

## Risks & Trade-offs

- **Single file:** Everything inline means no external CSS/JS files. This is actually a feature — it's one file to share.
- **No build tools:** Vanilla HTML is more accessible — works everywhere, no npm/node needed.
- **Photo placeholders:** We'll use gradient backgrounds as placeholders with clear instructions for replacing them.
- **Performance:** All animations are CSS-based (GPU-accelerated) for smooth performance on mobile.
