# Website Design Recreation

## Workflow

When the user provides a reference image (screenshot) and optionally some CSS classes or style notes:

1. **Generate** a single `index.html` file using Tailwind CSS (via CDN). Include all content inline — no external files unless requested.

2. **Render & Navigate (Playwright MCP)**
   - Use `mcp_playwright_browser_navigate` to open the generated `index.html`

3. **Screenshot**
   - Use `mcp_playwright_browser_screenshot`
   - Capture full page
   - Capture specific sections if needed

4. **Compare**
   Compare your screenshot against the reference image. Check for mismatches in:
   - Spacing and padding (measure in px)
   - Font sizes, weights, and line heights
   - Colors (exact hex values)
   - Alignment and positioning
   - Border radii, shadows, and effects
   - Responsive behavior
   - Image/icon sizing and placement

5. **Inspect (Playwright MCP)**
   - Use `mcp_playwright_browser_snapshot` to inspect DOM structure if needed

6. **Fix**
   - Edit the HTML/Tailwind code to resolve ALL mismatches

7. **Re-screenshot**
   - Repeat screenshot + compare

8. **Repeat Loop**
   - Continue steps 4–7 at least **2 full cycles**
   - Do NOT stop until:
     - Differences are within ~2–3px
     - Or user explicitly says stop

---

## Visual Validation Rules (MANDATORY)

IMMEDIATELY after implementing any UI:

- Always validate using Playwright
- Never assume visual correctness
- Always compare against reference image
- Always perform at least 2 validation passes

---

## Playwright MCP Commands

Use the following tools when needed:

- `mcp_playwright_browser_navigate`
- `mcp_playwright_browser_screenshot`
- `mcp_playwright_browser_snapshot`
- `mcp_playwright_browser_click`
- `mcp_playwright_browser_type`

---

## Technical Defaults

- Use Tailwind CSS via CDN:
  `<script src="https://cdn.tailwindcss.com"></script>`
- Use placeholder images from `https://placehold.co/` when source images aren't provided
- Mobile-first responsive design
- Single `index.html` file unless the user requests otherwise

---

## Rules

- Do not add features, sections, or content not present in the reference image
- Match the reference exactly — do not "improve" the design
- If the user provides CSS classes or style tokens, use them verbatim
- Keep code clean but don't over-abstract — inline Tailwind classes are fine

---

## Comparison Standards

When comparing screenshots, ALWAYS be specific:

Examples:
- "Heading is ~32px but should be ~24px"
- "Gap between cards is 16px but should be 24px"
- "Padding-left is 20px but reference shows ~32px"
- "Button radius is too large (should be ~6px)"

Avoid vague statements like:
- "Spacing is off"
- "Looks slightly different"

---

## Design System Alignment (Optional)

If `/rules/design-rules.md` exists:

- Ensure spacing scale consistency
- Follow typography hierarchy
- Match color tokens exactly
- Maintain consistent component styling
