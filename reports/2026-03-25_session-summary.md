# Session Summary — 2026-03-25

## Project: TrustedHealthGuideUSA

---

## Errors Found

### 1. All 15 images returning 404
- **Type:** Resource not found
- **Affected files:** `trustedlogo.png`, `fatlossbg3.png`, `refills.svg`, `directmeds.svg`, `sprout.svg`, `eden.svg`, `mochi.webp`, `medvi.png`, `remedy.png`, `willow.svg`, `prime.svg`, `jrn.svg`, `fridays.svg`, `trustedicon.png` (favicon)
- **Root cause:** Local server was being served from `project/TrustedHealthGuideUSA/` — the HTML uses `../../img/` relative paths, which resolve correctly only when the server runs from the project root (`newhealthguideproject/`)
- **Status:** ✅ Fixed by restarting server from root folder

### 2. `favicon.ico` 404
- **Type:** Browser default behavior
- **Root cause:** Browsers automatically request `/favicon.ico` even when a custom icon is declared via `<link rel="icon">`. Not a real error.
- **Status:** ✅ Ignored — expected behavior

### 3. Server redirect (301)
- **Type:** Navigation redirect
- **Detail:** `npx serve` redirects `/project/TrustedHealthGuideUSA/index.html` → `/project/TrustedHealthGuideUSA/`
- **Status:** ✅ Harmless — page loads correctly after redirect

---

## Tests Run

| Test | Session | Result |
|---|---|---|
| Image path check | `img-test` (headed) | ✅ All 17 images loaded |
| CTA Visit Site links | `cta-test` (headed) | ✅ All 11 links correct |

---

## CTA URLs Verified

| Brand | URL | Status |
|---|---|---|
| Refills | https://www.refills.com/weight-loss | ✅ |
| Direct Meds | https://directmeds.com/dm-offers-stc | ✅ |
| Sprout | https://joinsprouthealth.com/weightloss-k | ✅ |
| Eden | https://www.tryeden.com/treatment/glp-1-treatments | ✅ |
| Mochi | https://joinmochi.com/ | ✅ |
| MEDVi | https://glp.medvi.org/ | ✅ |
| Remedy Meds | https://remedymeds.com/ | ✅ |
| Willow | https://www.startwillow.com/ | ✅ |
| Prime Health | https://joinprimehealth.com/ | ✅ |
| Jrnys | https://jrnys.com/campaign/glp-1-membership-aff | ✅ |
| Fridays | https://www.joinfridays.com/ | ✅ |

---

## Learnings

1. **Always serve from the project root** — image paths like `../../img/` break when the server starts from a subfolder. Always run `npx serve` from `newhealthguideproject/`.
2. **`file://` protocol is blocked** by playwright-cli — always use a local HTTP server instead.
3. **`python -m http.server` is unavailable** on this machine — use `npx serve` instead.
4. **Two parallel headed sessions work** — use `-s=session-name --headed` to run multiple visible browser tests simultaneously.
5. **Screenshots folder structure:** Save all test screenshots to `screenshots/<ProjectName>/` with format `ProjectName_description_YYYY-MM-DD_HH-MM.png`.

---

## Screenshots
- `screenshots/TrustedHealthGuideUSA/TrustedHealthGuideUSA_initial-check_2026-03-25_14-42.png`
- `screenshots/TrustedHealthGuideUSA/TrustedHealthGuideUSA_image-test_2026-03-25_14-42.png`
- `screenshots/TrustedHealthGuideUSA/TrustedHealthGuideUSA_final-image-test_2026-03-25_14-42.png`
- `screenshots/TrustedHealthGuideUSA/TrustedHealthGuideUSA_final-cta-test_2026-03-25_14-42.png`
