# Design Principles (Health & Wellness Focus)

## Purpose
This design system ensures all UI reflects trust, clarity, and professionalism suitable for a health-related website.

All components MUST follow these standards.

---

## 1. Design Philosophy

- Clean, calm, and trustworthy
- Focus on readability and accessibility
- Informative over decorative
- Professional but approachable
- Avoid overly flashy or “techy” UI

---

## 2. Layout & Spacing

### Spacing Scale (Tailwind)
Use consistent spacing:

- 4px → `p-1`
- 8px → `p-2`
- 12px → `p-3`
- 16px → `p-4`
- 24px → `p-6`
- 32px → `p-8`
- 48px → `p-12`
- 64px → `p-16`

### Rules
- Use more breathing room than typical SaaS
- Sections should feel open and readable
- Prefer `py-12` to `py-16` for sections

---

## 3. Typography

### Style
- Clean sans-serif (Inter-style or system font)

### Scale
- Heading 1 → `text-3xl md:text-4xl font-bold`
- Heading 2 → `text-2xl md:text-3xl font-semibold`
- Heading 3 → `text-xl font-semibold`
- Body → `text-base leading-relaxed`
- Small → `text-sm text-gray-500`

### Rules
- Prioritize readability (important for health content)
- Use more line-height (`leading-relaxed`)
- Avoid overly bold or aggressive text

---

## 4. Colors (Trust-Based Palette)

### Base
- Background → `bg-white`
- Section background → `bg-gray-50`
- Text primary → `text-gray-900`
- Text secondary → `text-gray-600`
- Borders → `border-gray-200`

### Primary (Health Tone)
Use calming colors:
- Blue → `blue-600` (trust)
- Green → `green-600` (wellness)

### Example Usage
- Buttons → `bg-green-600 text-white`
- Links → `text-blue-600`

### Rules
- Avoid harsh or neon colors
- Keep palette soft and calm
- Maintain strong contrast for readability

---

## 5. Buttons

### Primary
- `bg-green-600 text-white px-5 py-2.5 rounded-lg`
- Hover → `bg-green-700`

### Secondary
- `border border-gray-300 text-gray-700 px-5 py-2.5 rounded-lg`

### Rules
- Clear CTA (e.g., “Learn More”, “Get Started”, “Read Guide”)
- Buttons should feel accessible and friendly

---

## 6. Cards & Content Blocks

### Card Style
- `bg-white border border-gray-200 rounded-xl p-6`

### Rules
- Minimal shadows (`shadow-sm` only if needed)
- Focus on content clarity
- Use cards for articles, tips, or guides

---

## 7. Borders & Radius

- Default → `rounded-lg`
- Cards → `rounded-xl`

### Rules
- Soft edges (not sharp)
- Consistent across all elements

---

## 8. Shadows

- Use very subtle shadows:
  - `shadow-sm` only

### Rules
- Avoid heavy shadows (not trustworthy for health UI)
- Keep UI flat and clean

---

## 9. Content Structure (IMPORTANT)

Health sites are content-heavy.

### Rules
- Break content into sections
- Use headings frequently
- Use bullet points for readability
- Avoid long dense paragraphs

---

## 10. Alignment & Layout

- Use `max-w-5xl mx-auto` for content width
- Keep text centered OR left-aligned consistently

### Patterns
- Article layout → centered with readable width
- Sections → spaced vertically with clear separation

---

## 11. Responsive Design

### Rules
- Mobile-first
- Stack content vertically on small screens
- Ensure text is readable without zoom

---

## 12. Images & Visuals

### Rules
- Use clean, relevant health imagery
- Avoid overly stocky or fake-looking images
- Maintain consistent sizes

### Placeholder
https://placehold.co/

---

## 13. Trust Signals (VERY IMPORTANT)

Include when possible:
- Author names
- Dates
- Medical disclaimers
- Sources or references

### Rules
- UI should feel credible and reliable

---

## 14. Interaction States

### Hover
- Subtle only (no dramatic effects)

### Focus
- Clear but soft focus states

---

## 15. Consistency Rules (CRITICAL)

- Same components = same styles
- Same spacing = same values
- No random design decisions

---

## 16. What to Avoid

- ❌ Flashy gradients
- ❌ Neon colors
- ❌ Overly modern SaaS UI
- ❌ Heavy animations
- ❌ Cluttered layouts
- ❌ Dense unreadable text

---

## 17. Validation Checklist

Before completing any UI:

- Readability is high
- Spacing feels open and clean
- Colors feel calm and trustworthy
- Content is well-structured
- Layout is consistent
- Mobile view is clean